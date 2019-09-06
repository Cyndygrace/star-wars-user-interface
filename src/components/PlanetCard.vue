<template>
<v-container class="ma-auto" fluid>
  <v-row :align="alignment" :justify="justify" class="grey lighten-5">
  <v-card
  hover
  tile
  elevation
  v-for="(planet, index) in planets"
  v-bind:key="index"
  v-if="index<=2"
  hover
    class="ma-1 pa-0 ma-8"
    outlined
    title
    max-width="390"
  >
    <v-img
    elevation
    hover
      class="white--text"
      height="400px"
      :src="`../assets/image/planet-${Math.ceil(Math.random()*3)}.jpg`"
    >
    <div class="mt-12 align-end fill-height">
      <v-card-title class="align-end my-12 mb-0 align-sm-content-end align-content-end" font-weight-bold>Name: {{planet.name}}</v-card-title><br />
      <span class="py-0 title align-end fill-height" font-weight-bold>Climate: {{planet.climate}}</span>
              <br />
              <span class="py-0 title align-end fill-height" font-weight-bold>Population: {{planet.population}}</span>
              <br />
</div>
    </v-img>

  </v-card>
  </v-row>
  </v-container>
</template>

<script>
export default {
  name:'PlanetCard',
  props: ["planets"],
  data() {
    return {
      alignmentsAvailable: ["start", "center", "end", "baseline", "stretch"],
      alignment: "center",
      dense: false,
      justifyAvailable: [
        "start",
        "center",
        "end",
        "space-around",
        "space-between"
      ],
      justify: "center"
    }
  }
}
</script>