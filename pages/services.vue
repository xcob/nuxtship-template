<script setup>
definePageMeta({
  layout: "landing",
});

const pricing = [
  {
    name: "Startup",
    price: {
      monthly: "Digital Marketing",
      annual: "$16",
      discount: "10%",
      original: "$24",
    },
    popular: true,
    features: [
      "All Free Features",
      "Up to 20 users",
      "20 Custom domains",
      "Unlimited Collaborators",
      "Advanced Integrations",
      "Priority Support",
    ],
    button: {
      text: "Get Started",
      link: "https://docs.google.com/forms/d/e/1FAIpQLSdUADj6R44NLNlGiqqvt96r_ocqwB7CR2jCsM2nUax5j9wOLg/viewform",
    },
  },
  {
    name: "Enterprise",
    price: "Web Development",
    popular: false,
    features: [
      "All Pro Features",
      "Unlimited Custom domains",
      "99.99% Uptime SLA",
      "SAML & SSO Integration",
      "Dedicated Account Manager",
      "24/7 Phone Support",
    ],
    button: {
      text: "Contact us",
      link: "https://docs.google.com/forms/d/e/1FAIpQLSdUADj6R44NLNlGiqqvt96r_ocqwB7CR2jCsM2nUax5j9wOLg/viewform",
    },
  },
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
