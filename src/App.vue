<template>
  <v-app>
    <Header />
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>
<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Montserrat&display=swap");

.application {
  font-family: "Montserrat";
}
</style>
<script>
import Header from "./components/Header";

export default {
  name: "App",
  components: {
    Header
  },

  data: () => ({})
};
</script>
