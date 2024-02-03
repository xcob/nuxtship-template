<template>
  <main class=" lg:grid-cols-2 place-items-center pt-16 pb-8 md:pt-8 hero">
    <div class="p-24 md:order-1 hidden md:block">
      <div class="tk-blob" style="--time: 20s; --amount: 5; --fill: #4e79fa">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 747.2 726.7">
          <path d="M539.8 137.6c98.3 69 183.5 124 203 198.4 19.3 74.4-27.1 168.2-93.8 245-66.8 76.8-153.8 136.6-254.2 144.9-100.6 8.2-214.7-35.1-292.7-122.5S-18.1 384.1 7.4 259.8C33 135.6 126.3 19 228.5 2.2c102.1-16.8 213.2 66.3 311.3 135.4z"></path>
        </svg>
      </div>
      <div class="tk-blob second-blob" style="--time: 10s; --amount: 5; --fill: #000411">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 747.2 726.7">
          <path d="M539.8 137.6c98.3 69 183.5 124 203 198.4 19.3 74.4-27.1 168.2-93.8 245-66.8 76.8-153.8 136.6-254.2 144.9-100.6 8.2-214.7-35.1-292.7-122.5S-18.1 384.1 7.4 259.8C33 135.6 126.3 19 228.5 2.2c102.1-16.8 213.2 66.3 311.3 135.4z"></path>
        </svg>
      </div>
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
          target="_blank" rel="noopener">Contact Us</LandingLink>
      </div>
    </div>
  </main>
</template>