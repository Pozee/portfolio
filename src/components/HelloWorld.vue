<template >
  <v-container fill-height class="d-flex align-center justify-center flex-column">
    <h1 class="display-4 text-center white--text">Pontus Zetterberg</h1>
    <h4 class="display-2 text-center font-weight-thin white--text">Frontend-utvecklare</h4>

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

    <v-btn x-large>
      mitt cv
      <v-icon right>mdi-text-box</v-icon>
    </v-btn>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({})
};
</script>
<style scoped>
</style>

