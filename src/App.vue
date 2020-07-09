<template >
  <v-app>
    <v-main style="background-color:#ecf0f1">
      <v-img max-height="100vh" src="./assets/laptop.jpg">
        <div class="makeDark">
          <HelloWorld />
        </div>
      </v-img>
      <maincontent class="main-content" />
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import maincontent from "./components/maincontent";
export default {
  name: "App",

  components: {
    HelloWorld,
    maincontent
  },

  data: () => ({
    //
  })
};
</script>

<style>
#social-icon:hover {
  color: rgb(201, 201, 201) !important;
}
.makeDark {
  position: relative;
  background-color: black;
  height: 100%;
  width: 100%;
  opacity: 0.8;
  top: 0;
  z-index: 1;
}
.main-content {
  height: 100vh;
}
#btn:hover {
  color: black !important;
}
</style>