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
              <h3>
                {{ items.projectTitle }} <span>{{ items.projectSoon }}</span>
              </h3>
              <p>{{ items.projectAbout }}</p>

              <div class="project__techstack">
                <img
                  :src="tech.img"
                  alt="Tech Stack"
                  v-for="(tech, index) in items.projectTech"
                  :key="index"
                />
              </div>
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
import hotelImg from "/src/assets/hotel.png";
export default {
  data() {
    return {
      quote:
        '"The journey of a thousand miles begins with one step." - Lao Tzu',

      projects: [
        {
          projectImage: unorkImg,
          projectTitle: "Unork Agency",
          projectAbout:
            "The website is an agency that turns dreams into reality and helps your business grow, this project focuses on user interface and user experience with navigation ease. ",
          projectLink: "https://unork-agency-website.vercel.app/",
          projectTech: [
            {
              img: "https://skillicons.dev/icons?i=vuejs",
            },
            {
              img: "https://skillicons.dev/icons?i=css",
            },
          ],
        },
        {
          projectImage: techTalkImg,
          projectTitle: "TechTalk Blog",
          projectSoon: "(Coming Soon)",
          projectAbout:
            "A website blog about technology, and let's you surf blogs, this project focuses on user friendly interface.",
          projectLink: "https://techtalk-blog.vercel.app/",
          projectTech: [
            {
              img: "https://skillicons.dev/icons?i=vuejs",
            },
            {
              img: "https://skillicons.dev/icons?i=scss",
            },
            {
              img: "https://skillicons.dev/icons?i=bootstrap",
            },
          ],
        },
        {
          projectImage: hotelImg,
          projectTitle: "Grand Standard",
          projectSoon: "(Coming Soon)",
          projectAbout:
            "A hotel website that the user can browse rooms, and dines. This project focuses on UI",
          projectLink: "https://grand-standard-hotel.vercel.app/",
          projectTech: [
            {
              img: "https://skillicons.dev/icons?i=vuejs",
            },
            {
              img: "https://skillicons.dev/icons?i=scss",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style></style>
