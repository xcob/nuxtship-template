<script setup>
onMounted(() => {
  const form = document.getElementById("form");
  const result = document.getElementById("result");

  form.addEventListener("submit", function (e) {
    e.preventDefault();
    form.classList.add("was-validated");
    if (!form.checkValidity()) {
      form.querySelectorAll(":invalid")[0].focus();
      return;
    }
    const formData = new FormData(form);
    const object = Object.fromEntries(formData);
    const json = JSON.stringify(object);

    result.innerHTML = "Sending...";

    fetch("https://api.web3forms.com/submit", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        Accept: "application/json",
      },
      body: json,
    })
      .then(async (response) => {
        let json = await response.json();
        if (response.status == 200) {
          result.classList.add("text-green-500");
          result.innerHTML = json.message;
        } else {
          console.log(response);
          result.classList.add("text-red-500");
          result.innerHTML = json.message;
        }
      })
      .catch((error) => {
        console.log(error);
        result.innerHTML = "Something went wrong!";
      })
      .then(function () {
        form.reset();
        form.classList.remove("was-validated");
        setTimeout(() => {
          result.style.display = "none";
        }, 5000);
      });
  });
});
</script>

<template>
  <!-- To make this contact form work, create your free access key from https://web3forms.com/
     Then you will get all form submissions in your email inbox. -->
  <form
    action="https://api.web3forms.com/submit"
    method="POST"
    id="form"
    class="needs-validation"
    novalidate
  >
    <input type="hidden" name="access_key" value="324bef96-e36e-41b1-be73-aa2fefa8a5d4" />
    <!-- Create your free access key from https://web3forms.com/ -->
    <input
      type="checkbox"
      class="hidden"
      style="display: none"
      name="botcheck"
    />
    <div class="mb-5">
      <input
        type="text"
        placeholder="Full Name"
        required
        class="w-full px-4 py-3 border-2 placeholder:text-gray-800 rounded-md outline-none focus:ring-4 border-gray-300 focus:border-gray-600 ring-gray-100"
        name="name"
      />
      <div class="empty-feedback invalid-feedback text-red-400 text-sm mt-1">
        Please provide your full name.
      </div>
    </div>
    <div class="mb-5">
      <label for="email_address" class="sr-only">Email Address</label
      ><input
        id="email_address"
        type="email"
        placeholder="Email Address"
        name="email"
        required
        class="w-full px-4 py-3 border-2 placeholder:text-gray-800 rounded-md outline-none focus:ring-4 border-gray-300 focus:border-gray-600 ring-gray-100"
      />
      <div class="empty-feedback text-red-400 text-sm mt-1">
        Please provide your email address.
      </div>
      <div class="invalid-feedback text-red-400 text-sm mt-1">
        Please provide a valid email address.
      </div>
    </div>
    <div class="mb-3">
      <label for="interest" class="">Services Needed</label
      >
      <ul class="items-center w-full text-sm font-medium text-gray-900 bg-white border  focus:ring-4 ring-gray-100  rounded-lg sm:flex ">
        <li class="w-full border-b border-gray-200 sm:border-b-0 sm:border-r ">
            <div class="flex items-center ps-3">
                <input id="vue-checkbox-list" type="checkbox" value="" name="Logo & Brand Design" class="w-4 h-4 text-blue-600 bg-gray-100  border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-700 dark:focus:ring-offset-gray-700 focus:ring-2 dark:bg-gray-600 ">
                <label for="vue-checkbox-list" class="w-full py-3 ms-2 text-sm font-medium">Logo & Brand Design</label>
            </div>
        </li>
        <li class="w-full border-b  sm:border-b-0 sm:border-r ">
            <div class="flex items-center ps-3">
                <input id="react-checkbox-list-2" type="checkbox" value="" name="Web Development" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-700 dark:focus:ring-offset-gray-700 focus:ring-2 dark:bg-gray-600 dark:border-gray-500">
                <label for="react-checkbox-list-2" class="w-full py-3 ms-2 text-sm font-medium">Web Development</label>
            </div>
        </li>
        <li class="w-full border-b sm:border-b-0 sm:border-r ">
            <div class="flex items-center ps-3">
                <input id="angular-checkbox-list-3" type="checkbox" value="" name="Social Media Graphics" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-700 dark:focus:ring-offset-gray-700 focus:ring-2 dark:bg-gray-600 dark:border-gray-500">
                <label for="angular-checkbox-list-3" class="w-full py-3 ms-2 text-sm font-medium ">Social Media Graphics</label>
            </div>
        </li>
      </ul>
    </div>
    <div class="mb-3">
      <textarea
        name="message"
        required
        placeholder="Your Message"
        class="w-full px-4 py-3 border-2 placeholder:text-gray-800 rounded-md outline-none h-36 focus:ring-4 border-gray-300 focus:border-gray-600 ring-gray-100"
      ></textarea>
      <div class="empty-feedback invalid-feedback text-red-400 text-sm mt-1">
        Please enter your message.
      </div>
    </div>
    <LandingButton type="submit" size="lg" block>Send Message</LandingButton>
    <div id="result" class="mt-3 text-center"></div>
  </form>
</template>

<style>
.invalid-feedback,
.empty-feedback {
  display: none;
}

.was-validated :placeholder-shown:invalid ~ .empty-feedback {
  display: block;
}

.was-validated :not(:placeholder-shown):invalid ~ .invalid-feedback {
  display: block;
}

.is-invalid,
.was-validated :invalid {
  border-color: #dc3545;
}
</style>
