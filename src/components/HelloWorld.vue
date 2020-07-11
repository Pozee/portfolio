<template >
  <v-container fill-height class="d-flex align-center justify-center flex-column">
    <h1 class="display-4 text-center white--text">Pontus Zetterberg</h1>
    <h4 class="display-2 text-center font-weight-thin white--text">Frontend-utvecklare</h4>
    <v-container class="d-flex justify-center">
      <v-btn x-large color="primary" id="btn" class="mr-4 ml-4">
        mitt cv
        <v-icon right color="white">get_app</v-icon>
      </v-btn>
      <v-btn
        class="project-btn"
        x-large
        color="white"
        outlined
        @click="$vuetify.goTo(target,options)"
      >
        Projekt & kompetens
        <v-icon class="project-icon" right>mdi-arrow-right</v-icon>
      </v-btn>
    </v-container>
    <v-container class="d-flex justify-center">
      <a href="https://www.linkedin.com/in/pontus-zetterberg-a2b739114/" target="_blank">
        <v-icon id="social-icon" x-large color="white" class="mr-1 ml-1">mdi-linkedin</v-icon>
      </a>

      <a href="https://github.com/Pozee" target="_blank">
        <v-icon id="social-icon" x-large color="white" class="mr-1 ml-1 social-icon">mdi-github</v-icon>
      </a>
      <a href="mailto:kontakt@pontuszetterberg.com" target="_blank">
        <v-icon id="social-icon" x-large color="white" class="mr-1 ml-1 social-icon">mdi-email-send</v-icon>
      </a>
    </v-container>
  </v-container>
</template>

<script>
import * as easings from "vuetify/es5/services/goto/easing-patterns";
export default {
  name: "HelloWorld",

  data: () => ({
    target: ".main-content",
    duration: 600,
    offset: 0,
    easing: "easeInOutCubic",
    easings: Object.keys(easings)
  })
};
</script>
<style scoped>
.project-btn {
  transition: ease-in-out 0.1;
}
.project-btn:hover .project-icon {
  padding-left: 5px;
  color: #f5f5f5;
}
#btn {
  border: solid transparent 1px !important;
}
#btn:hover {
  border: solid rgba(255, 255, 255, 0.808) 1px !important;
}
</style>

