<script setup>
definePageMeta({
  layout: "landing",
});

const TeamImg1 = "~/assets/img/kennedy-smith.png";
const TeamImg2 = "~/assets/img/jacob-smith.png";

const team = [
  {
    name: "Kennedy Smith",
    title: "Creative Director",
    avatar: {
      src: "~/assets/img/kennedy-smith.png",
      width: 480,
      height: 560,
    },
  },
  {
    name: "Jacob Smith",
    title: "Developer - Digital Strategist",
    avatar: {
      src: TeamImg2,
      width: 580,
      height: 580,
    },
  }
];
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>About</template>
      <template v-slot:desc>We are a small passionate team.</template>
    </LandingSectionhead>

    <div class="flex flex-col gap-3 mx-auto max-w-4xl mt-16">
      <h2 class="font-bold text-3xl">
        Boutique Creative Group
      </h2>
      <p class="text-lg leading-relaxed text-slate-500">
        We're a 
      </p>
    </div>
    <div class="grid md:grid-cols-2 gap-10 mx-auto max-w-4xl mt-12">
      <div class="group">
        <div class="w-full aspect-square">
          <img
            src="~/assets/img/kennedy-smith.png"
            width="450"
            height="450"
            format="avif"
            alt="Team"
            class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
          />
        </div>
        <div class="mt-4 text-center">
          <h2 class="text-lg text-gray-800">{{ team.name }}</h2>
          <h3 class="text-sm text-slate-500">{{ team.title }}</h3>
        </div>

      </div>
      <div class="group">
        <div class="w-full aspect-square">
          <img
            src="~/assets/img/jacob-smith.png"
            width="450"
            height="450"
            format="avif"
            alt="Team"
            class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
          />
        </div>
        <div class="mt-4 text-center">
          <h2 class="text-lg text-gray-800">{{ team.name }}</h2>
          <h3 class="text-sm text-slate-500">{{ team.title }}</h3>
        </div>
        </div>
      <!-- {
        team.map((item) => (
          <div class="group">
            <div class="w-full aspect-square">
              <Image
                {...item.avatar}
                format="avif"
                alt="Team"
                class="w-full h-full object-cover rounded transition  group-hover:-translate-y-1 group-hover:shadow-xl"
              />
            </div>

            <div class="mt-4 text-center">
              <h2 class="text-lg text-gray-800"> {item.name}</h2>
              <h3 class="text-sm text-slate-500"> {item.title}</h3>
            </div>
          </div>
        ))
      } -->
    </div>

    <div class="grid md:grid-cols-2 gap-10 mx-auto max-w-4xl mt-12">
      <div class="group">
        <div class="mt-4 text-center">
          <h2 class="text-lg text-gray-800">We are your Marketing Team</h2>
          <h3 class="text-sm text-slate-500">Empower your business with marketing strategies and assets.</h3>
        </div>

      </div>
      <div class="group">
        <div class="w-full">
          <img
            src="assets/img/marketing-about.png"
            width="800"
            height="450"
            format="avif"
            alt="Team"
            class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
          />
        </div>
        <div class="mt-4 text-center">
          <h2 class="text-lg text-gray-800">{{ team.name }}</h2>
          <h3 class="text-sm text-slate-500">{{ team.title }}</h3>
        </div>
        </div>
      
    </div>
  </LandingContainer>
</template>
