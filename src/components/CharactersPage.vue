<template>
  <div>
    <CharacterCard v-bind:characters="characters" />
  </div>
</template>

<script>
import CharacterCard from "../components/CharacterCard";
import axios from 'axios'
export default {
  name: "Characters",
  components: {
    CharacterCard
  },
  data() {
    return {
      characters: []
    };
  },
  created() {
    axios
      .get("https://swapi.co/api/people/?_limit=6")
      .then(res => (this.characters = res.data.results))
      .then(console.log(this.characters))
      .catch(error => console.log(error));
  }
};
</script>>