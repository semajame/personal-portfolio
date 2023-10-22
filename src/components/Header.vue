<template>
  <header>
    <slot> </slot>
    <div class="left__header">
      <a href="#" class="logo" v-scrollto="'home'">James.dev</a>
    </div>
    <div class="right__header">
      <nav>
        <ul>
          <li>
            <a
              href="#"
              v-for="(links, index) in navLinks"
              :key="index"
              :v-scrollto="links.scrollTo"
            >
              {{ links.link }}
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",

  data() {
    return {
      navLinks: [
        {
          link: "About",
          scrollTo: "'about'",
        },
        {
          link: "Projects",
          scrollTo: "'projects'",
        },
        {
          link: "Contact",
          scrollTo: "'contact'",
        },
      ],
    };
  },
};
</script>
