<template>
  <section class="projects__container" id="projects">
    <div class="projects__header">
      <div>
        <h2>Projects</h2>
        <span>💻</span>
      </div>
      <span class="quote"> {{ quote }}</span>
    </div>

    <div class="projects">
      <div class="projects__web__container">
        <div
          class="left__project"
          v-for="(items, index) in projects"
          :key="index"
        >
          <img
            :src="items.projectImage"
            alt="Project Image"
            class="project__image"
          />

          <div class="right__project">
            <h3>{{ items.projectTitle }}</h3>

            <p>{{ items.projectAbout }}</p>

            <div class="project__links">
              <a href="https://unork-agency-website.vercel.app/" target="_blank"
                >Live Demo <img src="/src/assets/arrow.svg" alt="Demo Arrow"
              /></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      quote:
        '"The journey of a thousand miles begins with one step." - Lao Tzu',

      projects: [
        {
          projectImage: "/src/assets/unork.png",
          projectTitle: "Unork Agency Website",
          projectAbout:
            "The website is an agency that turns dreams into reality and helps your business grow, this website focuses on user interface and user experience with navigation ease. ",
        },
      ],
    };
  },
};
</script>

<style></style>
