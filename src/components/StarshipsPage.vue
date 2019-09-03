<template>
  <div>
    <StarshipCard v-bind:starships="starships" />
  </div>
</template>

<script>
import StarshipCard from "../components/StarshipCard";
import axios from "axios";
export default {
  name: "Starships",
  components: {
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
      .then(console.log(this.starships))
      .catch(error => console.log(error));
  }
};
</script>>