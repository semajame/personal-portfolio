<template>
  <section class="projects__container" id="projects">
    <div class="projects__header">
      <div>
        <h2>Projects</h2>
        <span>💻</span>
      </div>
      <span class="quote"> {{ quote }}</span>
    </div>

    <div class="projects__main__container">
      <div class="projects" v-for="(items, index) in projects" :key="index">
        <div class="projects__web__container">
          <div class="left__project">
            <img
              :src="items.projectImage"
              alt="Project Image"
              class="project__image"
            />
            <div class="right__project">
              <h3>{{ items.projectTitle }}</h3>
              <p>{{ items.projectAbout }}</p>
              <div class="project__links">
                <a :href="items.projectLink" target="_blank"
                  >Live Demo <img src="/src/assets/arrow.svg" alt="Demo Arrow"
                /></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import unorkImg from "/src/assets/unork.png";
import techTalkImg from "/src/assets/techtalk.png";
export default {
  data() {
    return {
      quote:
        '"The journey of a thousand miles begins with one step." - Lao Tzu',

      projects: [
        {
          projectImage: unorkImg,
          projectTitle: "Unork Agency Website",
          projectAbout:
            "The website is an agency that turns dreams into reality and helps your business grow, this project focuses on user interface and user experience with navigation ease. ",
          projectLink: "https://unork-agency-website.vercel.app/",
        },
        {
          projectImage: techTalkImg,
          projectTitle: "TechTalk Blog",
          projectAbout:
            "The website is blog about technology, let's you surf on multiple blogs, this project focuses on user interface, and blog information with its own small database.",
          projectLink: "https://techtalk-blog.vercel.app/",
        },
      ],
    };
  },
};
</script>

<style></style>
