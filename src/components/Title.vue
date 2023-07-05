<template>
  <div className="section-title">
    <h2>{{ title }}</h2>
    <div className="underline"></div>
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true,
    default: "title",
  },
});
</script>
