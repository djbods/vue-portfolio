<template>
  <router-link
    v-for="(education, index) in educations"
    :key="index"
    to="/"
    class="blog"
  >
    <article>
      <img :src="education.image" class="blog-img" />
      <div class="blog-card">
        <h4>{{ education.title }}</h4>
        <p>{{ education.desc }}</p>
        <div class="blog-footer">
          <p>{{ education.category }}</p>
          <p>{{ education.date }}</p>
        </div>
      </div>
    </article>
  </router-link>
</template>

<script setup>
defineProps({
  id: {
    type: String,
    required: true,
    default: null,
  },
  title: {
    type: String,
    required: true,
    default: null,
  },
  date: {
    type: String,
    required: true,
    default: null,
  },
  category: {
    type: String,
    required: true,
    default: null,
  },
  desc: {
    type: String,
    required: true,
    default: null,
  },
  slug: {
    type: String,
    required: true,
    default: null,
  },
  image: {
    type: String,
    required: true,
    default: null,
  },
});

const educations = [
  {
    id: 1,
    title: "Holmesglen",
    date: "January 28th, 2021",
    category: "JavaScript",
    desc:
      "I completed a Diploma in Website Development at Holmesglen Moorabbin tafe. I received multiple distinctions for my projects and learned valuable skills and collected valuable online resources during my year at Holmesglen.",
    slug: "/",
    image: "https://www.clubchefstore.com.au/wp-content/uploads/2021/08/HG.jpg",
  },
  {
    id: 2,
    title: "SAE Institute",
    date: "May 4th, 2019",
    category: "Audio",
    desc:
      "I completed a Bachelor in Audio Engineering at SAE Institute in South Melbourne. The course is a three year course condensed into two years. I received multiple high distinctions whilst attending SAE.",
    slug: "/",
    image:
      "https://jack-bodsworth.netlify.app/static/af37f895e9667e87f5b8c6286ae52498/ee604/325a606dc2b6c68b59f25dc17818c0c5.png",
  },
  {
    id: 3,
    title: "McKinnon Secondary College",
    date: "January 28th, 2021",
    category: "Education",
    desc: "I completed my VCE at McKinnon Secondary College from 2011 - 2016.",
    slug: "/",
    image:
      "https://jack-bodsworth.netlify.app/static/98f3be49b1c0332d76c565cf64cc89f2/7bc87/b4f2ba347c3b894b6ef3d4a17d4ea075.jpg",
  },
];
</script>
