<template>
  <footer className="footer">
    <div>
      <SocialLinks styleClass="footer-links"></SocialLinks>
      {/*
      <h4>
        copyright &copy; {{ currentYear }} <span> WebDev</span> all rights
        reserved
      </h4>
      */}
    </div>
  </footer>
</template>

<script setup>
import { ref, onMounted } from "vue";

const currentYear = ref(null);

onMounted(() => {
  const date = new Date();
  currentYear.value = date.getFullYear();
});
</script>
