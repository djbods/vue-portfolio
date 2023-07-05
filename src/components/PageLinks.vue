<template>
  <ul class="page-links nav-links">
    <router-link :to="link.url" v-for="link in links" :key="link.id">
      {{ link.text }}
    </router-link>
  </ul>
</template>

<script setup>
const links = [
  {
    id: 1,
    text: "home",
    url: "/",
  },
  {
    id: 2,
    text: "about",
    url: "/about/",
  },
  {
    id: 3,
    text: "projects",
    url: "/projects/",
  },
  {
    id: 4,
    text: "education",
    url: "/education/",
  },
  {
    id: 5,
    text: "contact",
    url: "/contact/",
  },
];
</script>
