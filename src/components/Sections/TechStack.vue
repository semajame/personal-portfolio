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
            alt="Images"
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
  "   A technology stack is the foundation of your digital creation, like the building blocks and tools used to construct it. ";
const techStack = [
  {
    images: [
      {
        img: "https://skillicons.dev/icons?i=html",
      },
      {
        img: "https://skillicons.dev/icons?i=css",
      },
      {
        img: "https://skillicons.dev/icons?i=js",
      },
      {
        img: "https://skillicons.dev/icons?i=git",
      },
      {
        img: "https://skillicons.dev/icons?i=bootstrap",
      },
      {
        img: "https://skillicons.dev/icons?i=scss",
      },
      {
        img: "https://skillicons.dev/icons?i=tailwind",
      },
      {
        img: "https://skillicons.dev/icons?i=vuejs",
      },
    ],
  },
];
</script>
