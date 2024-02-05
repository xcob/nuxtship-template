<script setup>
definePageMeta({
  layout: "landing",
});

const TeamImg1 = "~/assets/img/kennedy-smith.png";
const TeamImg2 = "~/jacob-smith.png";

const team = [
  {
    name: "Bask & Bathe",
    title: "Home Spa Collective",
    avatar: {
      src: TeamImg1,
      width: 480,
      height: 560,
    },
  },
  {
    name: "The Knob Shoppe",
    title: "Homemade Guitar Pedals",
    avatar: {
      src: "~/assets/img/jacob-smith.png",
      width: 580,
      height: 580,
    },
  }
];
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Our Work</template>
      <template v-slot:desc>Our past clients success</template>
    </LandingSectionhead>

    <!-- sub heading -->
    <!-- <div class="flex flex-col gap-3 mx-auto max-w-4xl mt-16">
      <h2 class="font-bold text-3xl">
        Boutique Creative Group
      </h2>
      <p class="text-lg leading-relaxed text-slate-500">
        We're a 
      </p>
    </div> -->
    <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-4xl mt-12">
      <div v-for="item of team" class="group">
        <div class="w-full aspect-square">
          <img
            :src="TeamImg2"
            :width="item.avatar.width"
            :height="item.avatar.height"
            format="avif"
            alt="Team"
            class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
          />
        </div>

        <div class="mt-4 text-center">
          <h2 class="text-lg text-gray-800">{{ item.name }}</h2>
          <h3 class="text-sm text-slate-500">{{ item.title }}</h3>
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
  </LandingContainer>
</template>
