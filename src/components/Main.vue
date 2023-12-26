<template>
  <header>
    <div class="left__header">
      <a href="#" class="logo" v-scrollto="'home'" @click="toggleLogo">{{
        dev
      }}</a>
    </div>
    <div class="right__header">
      <nav>
        <ul id="ul">
          <li>
            <a
              href="#"
              v-for="(links, index) in navLinks"
              :key="index"
              v-scrollto="links.scrollTo"
            >
              {{ links.link }}
            </a>
          </li>
        </ul>
      </nav>
    </div>

    <label class="hamburger__container">
      <input type="checkbox" @click="toggleActive" id="checkbox" />
      <div class="checkmark">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </label>
  </header>
  <main id="home">
    <div class="hero__container">
      <div class="left__main">
        <h1>Front-End Web <br />Developer</h1>
        <p>
          {{ heroParagraph }}
        </p>
      </div>
      <div class="right__main">
        <img src="../assets/profile.jpg" alt="Profile" />
      </div>
    </div>
    <div class="tech__stack__container">
      <div class="tech__stack">
        <span> Tech Stack </span>
        <span>|</span>
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

          <div>
            <img
              :src="item.img"
              alt="Images"
              v-for="(item, index) in stack.imagesTwo"
              :key="index"
            />
          </div>
        </div>
      </div>
    </div>
  </main>

  <About id="about" />
  <Projects id="projects" />
  <Contacts id="contact" />
  <footer>
    <div>
      <a href="#" class="logo" v-scrollto="'home'">{{ dev }}</a>
      <p>{{ footerParagraph }}</p>
    </div>
  </footer>
</template>

<script>
import About from "../components/Sections/About.vue";
import Projects from "../components/Sections/Projects.vue";
import Contacts from "../components/Sections/Contacts.vue";

const scrollToDirective = {
  mounted(el, binding) {
    el.addEventListener("click", (event) => {
      event.preventDefault();
      const targetId = binding.value;
      const targetElement = document.getElementById(targetId);

      if (targetElement) {
        const offset = 100;
        const scrollTo = targetElement.offsetTop - offset;

        window.scrollTo({
          behavior: "smooth",
          top: scrollTo,
        });

        ul.classList.remove("active");
        checkbox.checked = false;
      }
    });
  },
};

export default {
  directives: {
    scrollto: scrollToDirective,
  },

  components: {
    About,
    Projects,
    Contacts,
  },

  methods: {
    toggleActive() {
      const ul = document.querySelector("#ul");
      ul.classList.toggle("active");
    },

    toggleLogo() {
      const ul = document.querySelector("#ul");
      const checkbox = document.querySelector("#checkbox");
      checkbox.checked = false;
      ul.classList.remove("active");
    },

    created() {
      const ul = document.querySelector("#ul");
      ul.addEventListener("click", this.toggleActive, this.toggleLogo);
    },
  },

  data() {
    return {
      dev: "James.dev",

      navLinks: [
        {
          link: "About",
          scrollTo: "about",
        },
        {
          link: "Projects",
          scrollTo: "projects",
        },
        {
          link: "Contact",
          scrollTo: "contact",
        },
      ],

      heroParagraph:
        "  Hi! I'm James Anquillano. A passionate Front-End Developer based in Cebu Philippines. 📍",

      footerParagraph: "Copyright © 2023. All rights are reserved",

      techStack: [
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
          ],

          imagesTwo: [
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
      ],
    };
  },
};
</script>
<style></style>
