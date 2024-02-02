<template>
  <main class="grid lg:grid-cols-2 place-items-center pt-16 pb-8 md:pt-8">
    <div class="p-24 md:order-1 hidden md:block">
      <img
        class="rounded-full transition-transform transform hover:scale-115"
        src="~/assets/img/smith-dots.png"
        alt="Starship starts the engine"
        loading="eager"
        format="avif"
        width="512"
        height="512"
      />
    </div>

    <div>
      <h1 class="text-5xl lg:text-6xl xl:text-7xl font-bold lg:tracking-tight">
        Marketing done right
      </h1>
      <p class="text-lg mt-4 text-slate-600 max-w-xl">
        Smith Creative is here to help you smash your business goals 
      </p>
      <div class="mt-6 flex flex-col sm:flex-row gap-3">
        <LandingLink
          href="https://docs.google.com/forms/d/e/1FAIpQLSdUADj6R44NLNlGiqqvt96r_ocqwB7CR2jCsM2nUax5j9wOLg/viewform"
          target="_blank"
          rel="noopener"
          >Contact Us</LandingLink
        >
      </div>
    </div>
  </main>
</template>
