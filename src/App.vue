<template>
  <div class="bg-[#111827] min-h-screen">
    <NavBar />
    <IntroductionSection />
    <ExperienceAndSkills />
    <LatestProjectsSection />
    <ContactSection />
    <Footer />
  </div>
</template>

<script setup>
import { defineAsyncComponent } from "vue";
// Import Components Asynchronously

const NavBar = defineAsyncComponent(() => import("@/components/NavBar.vue"));
const IntroductionSection = defineAsyncComponent(() =>
  import("@/components/IntroductionSection.vue")
);
const ExperienceAndSkills = defineAsyncComponent(() =>
  import("@/components/ExperienceAndSkills.vue")
);
const LatestProjectsSection = defineAsyncComponent(() =>
  import("@/components/LatestProjectsSection.vue")
);
const ContactSection = defineAsyncComponent(() =>
  import("@/components/ContactSection.vue")
);
const Footer = defineAsyncComponent(() => import("@/components/Footer.vue"));
</script>
