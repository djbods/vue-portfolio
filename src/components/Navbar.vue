<template>
  <nav class="navbar" style="margin-top: 0;">
    <div class="nav-center">
      <div class="nav-header">
        <span type="button" class="toggle-btn" @click="$emit('toggleSidebar')">
          <i class="fas fa-bars" />
        </span>
      </div>
      <PageLinks class="nav-links" />
    </div>
  </nav>
</template>

<script setup>
import PageLinks from "./PageLinks.vue";

defineEmits(["toggleSidebar"]);
</script>
