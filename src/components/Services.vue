<template>
  <section class="section bg-grey">
    <Title title="services"></Title>
    <div class="section-center services-center">
      <article v-for="service in services" :key="service.id" class="service">
        <h3><i style="height: 1.75em;" :class="service.icon"></i></h3>
        <h4>{{ service.title }}</h4>
        <div class="underline"></div>
        <p>{{ service.text }}</p>
      </article>
    </div>
  </section>
</template>

<script setup>
import Title from "./Title.vue";

const services = [
  {
    id: 1,
    title: "web development",
    text: `I'm a passionate front end web developer that aims to build a stunning platform on the latest and greatest technologies and frameworks available.`,
    icon: "fas fa-code",
  },
  {
    id: 2,
    title: "web design",
    text: `I can design front end websites using a variety of web design applications. I am most creative & proficient with Figma. `,
    icon: "fas fa-gem",
  },
  {
    id: 3,
    title: "music production ",
    text: `I've been producing, mixing and mastering electronic music for over 5 years now. I am also a professional dj that has played at thousands of events for a variety of different audiences.`,
    icon: "fas fa-music",
  },
];
</script>
