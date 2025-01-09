<template>
  <section class="text-white mt-18" id="skills">
    <div class="absolute right-0 top-[110rem] h-full w-full justify-end">
      <span class="flex opacity-20">
        <span class="w-16 h-32 rounded-full flex bg-primary blur-2xl"></span>
        <span
          class="w-16 h-32 rounded-full flex bg-[#f88fc2] blur-2xl mt-14"
        ></span>
      </span>
    </div>
    <div
      class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 xl:px-16"
    >
      <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[80%]">
        <h2 class="text-4xl font-bold text-white text-left mb-4">
          My
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary"
            >Skills</span
          >
        </h2>
        <div class="mt-8 grid grid-cols-3 gap-4">
          <div
            v-for="skill in skills"
            :key="skill.id"
            class="flex flex-col items-center"
          >
            <img :src="skill.logo" :alt="skill.name" class="w-16 h-16 mb-2" />
            <h4 class="font-semibold uppercase text-white text-center">
              {{ skill.name }}
            </h4>
          </div>
        </div>
      </div>
      <div data-aos="flip-left">
        <h2
          class="text-4xl font-bold text-white text-left mb-8 md:text-center md:mt-0 mt-8"
        >
          My
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary"
            >Experiences</span
          >
        </h2>
        <div class="space-y-8 py-8" data-aos="fade-left">
          <div
            v-for="experience in experiences"
            :key="experience.id"
            class="flex items-center rounded-xl p-4 bg-[#111a3e] shadow-lg border border-[#1f1641]"
          >
            <div class="w-1/4 mr-2 md:mr-4">
              <img
                src="https://img.icons8.com/ios-filled/100/ffffff/lawyer.png"
                alt="lawyer"
              />
            </div>
            <div class="w-3/4">
              <h3
                class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary"
              >
                {{ experience.role }}
              </h3>
              <p class="text-white">{{ experience.company }}</p>
              <p class="text-white">{{ experience.date }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const skills = ref([
  {
    id: 1,
    name: "HTML & CSS",
    logo: "https://img.icons8.com/color/96/html-5--v1.png",
  },
  {
    id: 2,
    name: "JavaScript",
    logo: "https://img.icons8.com/color/96/javascript--v1.png",
  },
  {
    id: 3,
    name: "React",
    logo: "https://img.icons8.com/plasticine/100/react.png",
  },
  {
    id: 4,
    name: "Next.js",
    logo: "https://img.icons8.com/color/100/ffffff/nextjs.png",
  },
  {
    id: 5,
    name: "Node.js",
    logo: "https://img.icons8.com/color/96/nodejs.png",
  },
  {
    id: 6,
    name: "Vue",
    logo: "https://img.icons8.com/color/96/vue-js.png",
  },
  {
    id: 7,
    name: "Nuxt.js",
    logo: "https://upload.wikimedia.org/wikipedia/commons/a/ae/Nuxt_logo.svg",
  },
  {
    id: 8,
    name: "Laravel",
    logo: "https://upload.wikimedia.org/wikipedia/commons/9/9a/Laravel.svg",
  },
  {
    id: 9,
    name: "Docker",
    logo: "https://img.icons8.com/color/96/docker.png",
  },
  {
    id: 10,
    name: "MySQL",
    logo: "https://img.icons8.com/color/96/mysql-logo.png",
  },
  {
    id: 11,
    name: "Git",
    logo: "https://img.icons8.com/color/96/git.png",
  },
  {
    id: 12,
    name: "GitHub",
    logo: "https://img.icons8.com/ios-glyphs/100/ffffff/github.png",
  },
  {
    id: 13,
    name: "Tailwind CSS",
    logo: "https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg",
  },
]);

const experiences = ref([
  {
    id: 1,
    role: "Web Developer",
    company: "France Solar",
    date: "Feb 2024 - Present",
  },
  {
    id: 2,
    role: "Web Developer",
    company: "France Solar",
    date: "Feb 2024 - Present",
  },
]);
</script>
