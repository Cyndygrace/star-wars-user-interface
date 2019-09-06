<template>
  <div>
    <Title v-bind:title="title3.text" />
    <CharacterCard v-bind:characters="characters" />
    <div class="text-center">
    <v-btn width ="600" class="ma-2 mt-0 pt-3 pb-9" tile outlined black>
      <v-icon >mdi-vuetify</v-icon> View More
    </v-btn>
    </div>
  </div>
</template>

<script>
import CharacterCard from "../components/CharacterCard";
import Title from "../components/Title";
import axios from 'axios'
export default {
  name: "PopularCharacters",
  props: ["title3"],
  components: {
    CharacterCard,
    Title
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
      .catch(error => error.message);
  }
};
</script>>