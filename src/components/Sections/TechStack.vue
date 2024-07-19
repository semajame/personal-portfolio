<template>
  <section id="tech__stack">
    <div class="tech__stack__container">
      <h2>Technology Stack</h2>
      <p class="tech__stack__p">
        {{ techP }}
      </p>
    </div>
    <div class="tech__stack">
      <div
        class="tech__flex"
        v-for="(stack, stackIndex) in techStack"
        :key="stackIndex"
      >
        <div>
          <img
            :src="item.img"
            :alt="item.alt"
            v-for="(item, index) in stack.images"
            :key="index"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const techP =
  "   A technology stack is the foundation of your digital creation, like the building blocks and tools used to construct it.";
const techStack = [
  {
    images: [
      {
        img: "https://skillicons.dev/icons?i=js",
        alt: "javascript",
      },

      {
        img: "https://skillicons.dev/icons?i=typescript",
        alt: "typescript",
      },
      {
        img: "https://skillicons.dev/icons?i=figma",
        alt: "figma",
      },
      {
        img: "https://skillicons.dev/icons?i=bootstrap",
        alt: "bootstrap",
      },
      {
        img: "https://skillicons.dev/icons?i=scss",
        alt: "scss",
      },
      {
        img: "https://skillicons.dev/icons?i=tailwind",
        alt: "tailwind",
      },
      {
        img: "https://skillicons.dev/icons?i=vuejs",
        alt: "vuejs",
      },
      {
        img: "https://skillicons.dev/icons?i=nuxt",
        alt: "nuxt",
      },
      // {
      //   img: "https://skillicons.dev/icons?i=express",
      //   alt: "expressjs",
      // },
      // {
      //   img: "https://skillicons.dev/icons?i=mysql",
      //   alt: "mysql",
      // },
    ],
  },
];
</script>
