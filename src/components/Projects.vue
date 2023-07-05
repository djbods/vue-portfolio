<template>
  <section class="section projects">
    <Title title="Featured Projects" />
    <div class="section-center projects-center">
      <Project
        v-for="project in projects"
        :key="project.id"
        :id="project.id"
        :description="project.description"
        :title="project.title"
        :url="project.url"
        :image="project.image"
      />
    </div>
    <router-link v-if="isHomePage" to="/projects" class="btn center-btn">
      projects
    </router-link>
  </section>
</template>

<script setup>
import { computed } from "vue";
import { useRoute } from "vue-router";

import Title from "./Title.vue";
import Project from "./Project.vue";

const projects = [
  {
    id: 1,
    description:
      "Planning, designing, developing and testing of new online training platform components using VueJs. This project was a complete overhaul of the previous legacy portal all students of the college used. The new online training portals purpose is to progress students through their exams, allow them to book, track and maintain their placements, create logbook entries, come up with learning development plans with their supervisors, enter their leave period. Other features of the platform include a system to track and discuss interruptions, trainee progress reviews for supervisor / admin roles and a trainee page that allows administrators to view a summary of any searched trainee and administrate their uploaded documents, leave comments and view other requirements.",
    title: "ACEM Learning Portal",
    image:
      "https://az659834.vo.msecnd.net/eventsairaueprod/production-acem-public/10b5ad42b4134384abb1524a917c57af",
  },
  {
    id: 2,
    description:
      "Self Storage business located in Richmond & Flemington, Melbourne. I am the website designer and developer. I have designed this website on React / Gatsby for the front end, using airtable to store data on the back end. The website will be hosted on AWS and the email system will be using MailChimp.",
    title: "Citlinked Self Storage",
    image:
      "https://www.citilinkedselfstorage.com.au/wp-content/uploads/2017/11/IMG_7451-compressed.jpg",
  },
  {
    id: 3,
    description:
      "I designed a profile finder using React.js as the front end, redux as the state management and firebase to store and access all the data rendering in React.js.",
    title: "React Redux Project",
    image:
      "https://www.educative.io/cdn-cgi/image/f=auto,fit=contain,w=1200/api/page/5186775737696256/image/download/6611525209948160",
  },
];

const isHomePage = computed(() => {
  const route = useRoute();
  return route.path === "/";
});
</script>
