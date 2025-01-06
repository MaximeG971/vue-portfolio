<template>
  <div class="bg-[#111827] min-h-screen">
    <!-- Wrap components in Suspense to handle loading -->
    <Suspense>
      <template #default>
        <!-- Wrap all Components inside a single root element -->
        <div>
          <NavBar />
          <IntroductionSection />
          <ExperienceAndSkills />
          <LatestProjectsSection />
          <ContactSection />
          <Footer />
          <BackToTop />
        </div>
      </template>
      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner />
        </div>
      </template>
    </Suspense>
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
const BackToTop = defineAsyncComponent(() =>
  import("@/components/BackToTop.vue")
);
const LoadingSpinner = defineAsyncComponent(() =>
  import("@/components/LoadingSpinner.vue")
);
</script>
