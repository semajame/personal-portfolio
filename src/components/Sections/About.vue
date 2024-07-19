<template>
  <section class="about__container" id="about">
    <div class="left__about laptop"></div>
    <div class="right__about">
      <div>
        <h2>About Me</h2>
        <span>👋🏽</span>
      </div>

      <p>
        {{ firstPara }}
        <br />
        <br />

        {{ secondPara }}
      </p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      firstPara:
        "Hi! I'm a passionate Frontend Developer from Cebu, Philippines. I specialize in crafting visually appealing and user-friendly interfaces with the use of my technology stack.",

      secondPara:
        "  My dedication to frontend development thrives on the dynamic challenges of staying at the forefront of technology. I also like to stay in the latest of technology, and learn about them more on my free time. I am currently making my thesis project using Angular.",
    };
  },
};
</script>
