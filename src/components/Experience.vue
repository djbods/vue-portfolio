<template>
  <section class="section jobs">
    <Title title="experience" />
    <div class="jobs-center">
      <div class="btn-container">
        <button
          v-for="(job, index) in jobs"
          :key="index"
          @click="toggleJob(index)"
          :class="['job-btn', { 'active-btn': index === selectedJobIndex }]"
        >
          {{ job.company }}
        </button>
      </div>
      <article v-if="selectedJob" class="job-info">
        <h3>{{ selectedJob.position }}</h3>
        <h4>{{ selectedJob.company }}</h4>
        <p class="job-date">{{ selectedJob.date }}</p>

        <div
          v-for="(description, index) in selectedJob.description"
          :key="index"
          class="job-desc"
        >
          <li>{{ description.value }}</li>
        </div>
      </article>
    </div>
    <router-link to="/about" class="btn center-btn">
      more info
    </router-link>
  </section>
</template>

<script setup>
import { ref, onMounted } from "vue";
import Title from "./Title.vue";

const selectedJob = ref(null);
const selectedJobIndex = ref(0);

const toggleJob = (index) => {
  selectedJob.value = jobs[index];
  selectedJobIndex.value = index;
  console.log(selectedJob.value, selectedJobIndex.value);
};

const jobs = [
  {
    jobId: 1,
    company: "ACEM",
    date: "Jul 2021 - Jul 2023",
    position: "Front-end Developer",
    description: [
      {
        id: 1,
        value:
          "Planning and designing of components of the ACEM training portal",
      },
      {
        id: 2,
        value:
          "Development of site logic and behaviour using VueJs and JavaScript",
      },
      {
        id: 3,
        value:
          "Participation in code review of other developers work via pull requests",
      },
    ],
  },
  {
    jobId: 2,
    company: "Tindoland",
    date: "July 2020 - Nov 2020",
    position: "Developer",
    description: [
      {
        id: 1,
        value:
          "Planning, designing, development and testing of Tindoland’s restaurant website using Wordpress CMS.",
      },
      {
        id: 2,
        value:
          "Liasing with client to ensure their business requirements were clear, concise and feasible for the technology and tools used.",
      },
    ],
  },
  {
    jobId: 3,
    company: "Citilinked Self Storage",
    date: "June 2020 - June 2022",
    position: "Front-end developer / UI-UX",
    description: [
      {
        id: 1,
        value:
          "Planning, designing and development of their website in ReactJS.",
      },
      {
        id: 2,
        value:
          "Changing the user flow of the site to ensure customers user experience was optimal in order for them to access the information, products & services they required.",
      },
      {
        id: 3,
        value:
          "Ensuring the site was accessible for all users by using scalable text and alternative text for images. Using colour contrasting was also key to this.",
      },
    ],
  },
];

onMounted(() => {
  selectedJob.value = jobs[0]; // Set the first job as the default
});
</script>
