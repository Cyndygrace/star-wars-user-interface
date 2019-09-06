<template>
  <v-container class="ma-auto" fluid>
    <v-row :align="alignment" :justify="justify" class="grey lighten-5">
      <v-card
        hover
        tile
        max-width="390"
        v-for="(starship, index) in starships"
        v-bind:key="index"
        v-if="index<=5"
        class="ma-1 pa-0 ma-8"
        outlined
        title
      >
        <v-img class="white--text" height="200px" :src="`../assets/image/starship-${Math.ceil(Math.random()*6)}.jpg`"></v-img>
        <div class="pb-2 grey lighten-1">
          <div class="grey lighten-2 ml-2 mr-n2">
            <v-card-text class="justify-content">
              <v-card-title
                class="title font-weight-bold text--primary pt-0 pb-0 pl-0"
              >Name: {{starship.name}}</v-card-title>
              <br />
              <span class="py-0 subtitle-1">Model: {{starship.starship_class}}</span>
              <br />
              <span class="py-0 subtitle-1">Capacity: {{starship.cargo_capacity}}</span>
              <br />
            </v-card-text>
            <div class="d-flex justify-end pr-3 pb-1">
              <v-card-actions>
                <div class="text-right pl-0">
                  <div class="flex-grow-1"></div>
                  <v-btn depressed large tile class="grey lighten-1 px-7">
                    <span class="overline">Read more</span>
                    <v-icon x-small left>mdi-arrow-right</v-icon>
                  </v-btn>
                </div>
              </v-card-actions>
            </div>
          </div>
        </div>
      </v-card>
    </v-row>
  </v-container>
</template>


<script>
export default {
  name: "StarshipCard",
  props: ["starships"],
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
    };
  },
  
};
</script>

<style scoped>
</style>
