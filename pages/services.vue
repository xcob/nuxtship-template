<script setup>
definePageMeta({
  layout: "landing",
});

const pricing = [
  {
    name: "Business Package",
    price: {
      monthly: "$1000/Month",
      annual: "$10k/Year",
      discount: "15%",
      original: "$12K",
    },
    popular: true,
    features: [
      "Lightening Fast Website",
      ""
    ],
    button: {
      text: "Get Started",
      link: "https://docs.google.com/forms/d/e/1FAIpQLSdUADj6R44NLNlGiqqvt96r_ocqwB7CR2jCsM2nUax5j9wOLg/viewform",
    },
  },
  {
    name: "Empower Your Business",
    price: "Web Development",
    popular: false,
    features: [
      "Custom Website Design",
    ],
    button: {
      text: "Contact us",
      link: "https://docs.google.com/forms/d/e/1FAIpQLSdUADj6R44NLNlGiqqvt96r_ocqwB7CR2jCsM2nUax5j9wOLg/viewform",
    },
  },
  {
    name: "Start Your Brand",
    price: {
      monthly: "Logo & Brand Design",
      annual: "$16",
      discount: "10%",
      original: "$24",
    },
    popular: true,
    features: [
      "Unrivaled branding",
    ],
    button: {
      text: "Get Started",
      link: "https://docs.google.com/forms/d/e/1FAIpQLSdUADj6R44NLNlGiqqvt96r_ocqwB7CR2jCsM2nUax5j9wOLg/viewform",
    },
  }
];
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Services</template>
      <template v-slot:desc
        >Boutique Offerings</template
      >
    </LandingSectionhead>

    <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-screen-lg mt-12">
      <LandingPricing v-for="item of pricing" :plan="item" />
    </div>
  </LandingContainer>
</template>
