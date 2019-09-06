<template>
<v-container class="ma-12 ml-12 mb-0" fluid>
  <v-row :align="alignment" :jsutify="justify" class="grey lighten-5">
  
    <!-- <div v-bind:key="character.id" v-for="character in characters">
      <v-row class="mx-auto ml-12"> -->

        <v-card 
        hover 
        tile
        class="ma-1 py-0 ma-8 pa-0 " 
        max-height='390' min-width="700" max-width='700'
        v-for="(character, index) in characters"
        v-bind:key="index"
        v-if="index <= 3"
        outlined
        title
        >
          
            <v-row>
              <v-img class="my-0 " max-width="400" height='390' :src="`../assets/image/character-${Math.ceil(Math.random()*4)}.jpg`"></v-img>
            
            <v-col>
              <v-card-text class="pb-0">
                <p class="title font-weight-bold text--primary mb-0">Name: {{character.name}}</p>
                <div class="mb-4">Year: {{character.birth_year}}</div>

                <div class="text--primary">Gender: {{character.gender}}</div>
              </v-card-text>
              <v-card-actions class="pt-0 pb-0">
                <v-btn text small class=" white lighten-5">Read More</v-btn>
              </v-card-actions>
              <v-divider
                class=" ml-2 pt-1 black mt-0"
                style="opacity: 4"
                role="seperator"
                width="100"
                aria-orientation="horizontal"
              ></v-divider>
            </v-col>
          </v-row>
        </v-card>
      <!-- </v-row> -->
    <!-- </div> -->
  
  </v-row>
</v-container>
</template>

<script>
export default {
  name: "CharacterCard",
  props: ["characters"],
  data() {
    return {
alignmentsAvailable:["start", "center", "end", "baseline", "stretch"],
alignment: "center",
dense: false,
jsutifyAvailable: [
  "start",
  "center",
  "end",
  "space-around",
  "space-between"
]
    }
  }
};
</script>>