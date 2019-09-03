<template>
  <div class="home">
    <Title v-bind:title="title1.text" />

    <StarshipsPage/>

    <Title v-bind:title="title2.text" />
    
        <PlanetsPage />

    <Title v-bind:title="title3.text" />

    <CharactersPage />
  </div>
</template>

<script>
import Title from "../components/Title";
import CharactersPage from '../components/CharactersPage'
import StarshipsPage from "../components/StarshipsPage";
import PlanetsPage from "../components/PlanetsPage";


export default {
  name: "Home",
  components: {
    Title,
    CharactersPage,
    StarshipsPage,
    PlanetsPage
  },
  data() {
    return {
      title1: { text: "Popular Starship" },
      title2: { text: "Popular Planets" },
      title3: { text: "Popular Characters" },
    
      header: { text: "Things To Do" }
    };
  }

};
</script>

