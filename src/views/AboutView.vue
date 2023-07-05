<template>
  <section className="about-page">
    <div className="section-center about-center">
      <img src="../assets/hero-img-jack.png" class="about-img" />
      <article className="about-text">
        <Title title="About me" />
        <p>{{ about }}</p>
        <div className="about-stack">
          <span v-for="item in stack" :key="item.id">{{ item.title }}</span>
        </div>
      </article>
    </div>
  </section>
</template>

<script setup>
import Title from "../components/Title.vue";

const about =
  "Im a Melbourne based web developer with a passion for creating beautiful front-end platforms for websites that stand above in the digital era. I studied at Holmesglen Institute and completed a Diploma in Website Development. The technologies I am proficient in are: React.js, Gatsby.js, Vue.js, JavaScript, HTML, CSS, Node.js, SASS and styled components. Additionally I am a music producer, DJ and audio engineer. I have a passion for composing, mixing, mastering and sharing electronic dance music. I completed a Bachelor of Audio Engineering at SAE Institute Melbourne from 2017 - 2019.";

const stack = [
  {
    id: 1,
    title: "html",
  },
  {
    id: 2,
    title: "css",
  },
  {
    id: 3,
    title: "javascript",
  },
  {
    id: 4,
    title: "vuejs",
  },
  {
    id: 5,
    title: "reactjs",
  },
  {
    id: 6,
    title: "nodejs",
  },
  {
    id: 7,
    title: "figma",
  },
];
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
