<template>
  <aside class="sidebar">
    <button @click="$emit('hideSidebar')" class="close-btn">
      X
    </button>
    <div class="side-container">
      <SidebarLinks @click="$emit('hideSidebar')" />
    </div>
  </aside>
</template>

<script setup>
import SidebarLinks from "./SidebarLinks.vue";

defineEmits(["hideSidebar"]);
</script>
