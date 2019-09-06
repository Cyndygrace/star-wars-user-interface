<template>
  <div>
    <Title v-bind:title="title2.text" />
    <PlanetCard v-bind:planets="planets" />
    
  </div>
</template>

<script>
import PlanetCard from "../components/PlanetCard";
import Title from "../components/Title";
import axios from 'axios'
export default {
  name: "Planets",
  props: ["title2"],
  components: {
    Title,
    PlanetCard
  },
  data() {
    return {
      planets: []
    };
  },
  created() {
  axios.
  get("https://swapi.co/api/planets/?_limit=6")
  .then(res => (this.planets = res.data.results))
  .catch(error => error);
  }
};
</script>>