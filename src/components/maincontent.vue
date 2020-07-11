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
            max-width="100"
            max-height="100"
            min-width="100"
            :src="loadPic(image.src)"
          ></v-img>
        </v-container>
      </v-card>
    </v-container>

    <v-container class="mt-10"></v-container>
  </v-container>
</template>

<script>
export default {
  name: "maincontent",
  data: () => ({
    images: [
      {
        src: "javascript.svg"
      },
      {
        src: "angularjs.svg"
      },
      {
        src: "vuejs.svg"
      },
      {
        src: "react.svg"
      },
      {
        src: "css.svg"
      },
      {
        src: "html5.svg"
      },
      {
        src: "firebase.svg"
      },
      {
        src: "logo-redux.png"
      }
    ],
    projects: [
      {
        name: "Webshop koncept för att köpa kaffe",
        tech: "Vanilla Javascript, CSS & HTML",
        type: "Grupparbete",
        github: "www.google.se",
        liveView: "www.twitch.tv"
      }
    ]
  }),
  methods: {
    loadPic(pic) {
      return require("../assets/" + pic);
    }
  }
};
</script>

<style scoped>
</style>