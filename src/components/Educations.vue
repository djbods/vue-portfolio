<template>
  <section className="section educations">
    <Title title="Education" />
    <div className="section-center blogs-center">
      <Education />
    </div>
    <router-link v-if="isHomePage" to="/education" className="btn center-btn"
      >Education</router-link
    >
  </section>
</template>

<script setup>
import { computed } from "vue";
import { useRoute } from "vue-router";

import Title from "./Title.vue";
import Education from "./Education.vue";

const isHomePage = computed(() => {
  const route = useRoute();
  return route.path === "/";
});
</script>
