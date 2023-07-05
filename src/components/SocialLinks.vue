<template>
  <router-link
    v-for="(icon, index) in data"
    :key="index"
    :to="icon.url"
    class="social-link"
  >
    <i :key="data.icon" :class="icon.name"></i>
  </router-link>
</template>

<script setup>
const data = [
  {
    id: 1,
    name: "fa-brands fa-facebook",
    url: "https://www.facebook.com/djbods1",
  },
  {
    id: 2,
    icon: "fa-brands fa-linkedin",
    url: "https://www.linkedin.com/in/jack-bodsworth-497a5453/",
  },
  {
    id: 3,
    icon: "fa-brands fa-github",
    url: "https://github.com/djbods",
  },
];
</script>
