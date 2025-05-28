<template>
  <main class="flex-grow border-0  ">
    <Hero />
    <BellowHero />
    <Services />
    <SCSL />
    <TechnologyUsed />
  </main>
</template>
<script setup lang="ts">
import Hero from "@/components/landing/Hero.vue";
import BellowHero from "@/components/landing/BellowHero.vue";
import Services from "@/components/landing/Services.vue";
import SCSL from "@/components/landing/SCSL.vue";
import TechnologyUsed from "@/components/landing/TechnologyUsed.vue";
useHead({
  title: "",
  meta: [
    {
      property: "og:title",
      content: "",
    },
    {
      property: "og:description",
      content: "Explore my projects and skills as a full stack developer.",
    },
  ],
});
</script>


