<template>
  <div>
    <Title v-bind:title="title1.text" />
    <StarshipCard v-bind:starships="starships" />
    <div class="text-center">
    <v-btn width ="600" class="ma-2 mt-0 pt-3 pb-9" tile outlined black>
      <v-icon >mdi-vuetify</v-icon> View More
    </v-btn>
  </div>
  </div>
</template>

<script>
import StarshipCard from "../components/StarshipCard";
import Title from "../components/Title";
import axios from "axios";
export default {
  name: "Starships",
  props: ["title1"],
  components: {
    Title,
    StarshipCard
  },
  data() {
    return {
      starships: []
    };
  },
  created() {
    axios
      .get("https://swapi.co/api/starships/?_limit=6")
      .then(res => (this.starships = res.data.results))
      
      .catch(error => error.message);
  }
};
</script>>