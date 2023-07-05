<template>
  <article class="project">
    <img :src="image" class="project-img" />
    <div class="project-info">
      <span class="project-number">{{ id }}.</span>
      <h3>{{ title }}</h3>
      <p class="project-description">{{ description }}</p>
      <div class="project-links"></div>
    </div>
  </article>
</template>

<script setup>
defineProps({
  id: {
    type: [String, Number],
    required: true,
    default: 0,
  },
  title: {
    type: String,
    required: true,
  },
  github: {
    type: String,
    required: true,
    default: "https://www.github.com",
  },
  image: {
    type: String,
    required: true,
    default: null,
  },
  url: {
    type: String,
    required: true,
    default: "https://www.google.com",
  },
  description: {
    type: String,
    required: true,
    default: "desc",
  },
  // stack: {
  //   type: Array,
  //   required: true,
  //   default: null,
  // },
});
</script>
