<template>
  <v-app>
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
export default {
  name: "App",
  data: () => ({})
};
</script>
