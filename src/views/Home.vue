<template>
  <div class="home">
    <Header />
    <PopularStarships v-bind:title1 = "title1" />
    <PopularPlanets v-bind:title2 = "title2" />
    <PopularCharacters v-bind:title3 = 'title3' />
    

    <!-- <Title v-bind:title="title2.text" />
    <PlanetsPage />
    <Title v-bind:title="title3.text" />

    <CharactersPage />-->
  </div>
</template>

<script>
import Header from "../components/Header";

import PopularStarships from "../components/PopularStarships";
import PopularPlanets from "../components/PopularPlanets";
import PopularCharacters from "../components/PopularCharacters";


export default {
  name: "Home",
  components: {
    
    Header,
    PopularCharacters,
    PopularPlanets,
    PopularStarships
  },
  data() {
    return {
      title1: { text: "Popular Starship" },
      title2: { text: "Popular Planets" },
      title3: { text: "Popular Characters" },
    };
  }
};
</script>

