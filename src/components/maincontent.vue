<template>
  <v-container>
    <v-container class="d-flex justify-center">
      <v-card color="white" class="elevation-3 d-flex-column" width="75em">
        <h2
          class="text-center display-1 text-uppercase font-weight-bold pt-5"
        >Blandad kompetens inom</h2>
        <v-container class="d-flex justify-center flex-wrap pb-10">
          <v-img
            v-for="image in images"
            :key="image.img"
            contain
            class="ml-5 mr-5 mt-5 mb-5"
            max-width="75"
            max-height="75"
            min-width="75"
            :src="loadPic(image.src)"
          ></v-img>
        </v-container>
      </v-card>
    </v-container>
    <v-card>
      <h2 class="text-center display-1 text-uppercase font-weight-bold pt-5">Mina projekt</h2>
      <v-container class="mt-4 d-flex flex-wrap justify-center">
        <v-card
          v-for="project in projects"
          :key="project.name"
          width="25em"
          class="elevation-3 ma-2"
        >
          <v-img
            class="white--text align-end justify-center"
            height="200px"
            :src="project.imgPreview"
          >
            <v-container class="d-flex justify-center">
              <a :href="project.github" target="_blank" class="mr-1">
                <v-icon color="white" size="50px" class="project-icon">mdi-github</v-icon>
              </a>

              <a :href="project.liveView" target="_blank">
                <v-icon color="white" size="50px" class="project-icon">preview</v-icon>
              </a>
            </v-container>
            <v-card-title class="title">{{project.name}}</v-card-title>
          </v-img>

          <v-container class="d-flex-column">
            <v-container class="pa-0 d-flex justify-space-between pl-1 pr-1">
              <span class="font-weight-thin">{{project.tech}}</span>
              <span class="font-weight-thin">{{project.type}}</span>
            </v-container>
          </v-container>
        </v-card>
      </v-container>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "maincontent",
  data: () => ({
    images: [
      {
        src: "javascript.svg",
      },
      {
        src: "angularjs.svg",
      },
      {
        src: "vuejs.svg",
      },
      {
        src: "react.svg",
      },
      {
        src: "css.svg",
      },
      {
        src: "html5.svg",
      },
      {
        src: "firebase.svg",
      },
      {
        src: "logo-redux.png",
      },
    ],
    projects: [
      {
        name: "Kopia av Hästens startsida",
        tech: "Vue.js, CSS & HTML",
        type: "Solo",
        github: "https://github.com/Pozee/hastens-homepage",
        liveView: "https://pozee.github.io/hastens-homepage/",
        imgPreview: "https://i.imgur.com/V62n9cu.jpg",
      },
      {
        name: "Livechat & autentisering via email",
        tech: "Vue.js, Firebase, CSS & HTML",
        type: "Solo",
        github: "https://github.com/Pozee/hastens-homepage",
        liveView: "https://pozee.github.io/hastens-homepage/",
        imgPreview: "https://i.imgur.com/52BOij3.png",
      },
      {
        name: "Genererar dadjokes och har sökfunktion",
        tech: "Javascript, CSS & HTML",
        type: "Solo",
        github: "https://github.com/Pozee/Dad-joke-generator",
        liveView: "https://pozee.github.io/Dad-joke-generator/",
        imgPreview: "https://i.imgur.com/bekDP01.png",
      },
      {
        name: "Webshop Kaffe",
        tech: "CSS & HTML",
        type: "Grupparbete",
        github: "https://github.com/Pozee/Projektarbete-Grupp2",
        liveView: "https://pozee.github.io/Projektarbete-Grupp2/",
        imgPreview: "https://i.imgur.com/Sj34rmp.jpeg",
      },
      {
        name: "Angular projekt",
        tech: "Javascript(Angular), CSS & HTML",
        type: "Solo",
        github: "https://github.com/Pozee/saloon-app",
        liveView: "https://pozee.github.io/saloon-app/",
        imgPreview: "https://i.imgur.com/PC6wbKC.png",
      },
      {
        name: "Mitt portfolio",
        tech: "Javascript(Vue,js),Vuetify, Vuex, CSS & HTML",
        type: "Solo",
        github: "https://github.com/Pozee/portfolio",
        liveView: "https://pontuszetterberg.com",
        imgPreview: "https://i.imgur.com/4N9QuqQ.jpg",
      },
    ],
  }),
  methods: {
    loadPic(pic) {
      return require("../assets/" + pic);
    },
  },
};
</script>

<style scoped>
.project-icon {
  cursor: pointer;
  color: rgb(216, 216, 216) !important;
  opacity: 1;
}
.project-icon:hover {
  color: rgb(156, 156, 156) !important;
}
a {
  text-decoration: none !important;
}
.title {
  padding: 0;
  padding-left: 0.5em;
  background-color: rgb(182, 182, 182);
}
</style>