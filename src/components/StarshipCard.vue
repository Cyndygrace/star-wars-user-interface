<template>
  <div>
    <div v-bind:key="starship.name" v-for="starship in starships">
      <v-row class="mx-auto ml-12">
        <!-- <v-col> -->
        <v-container fluid>
          <v-row
            :align="alignment"
            :justify="justify"
            class="grey lighten-5"
            style="height: 300px;"
          >
            <v-card hover 
            
            max-width="350" 
            v-for='n in 3'
            :key='n'
            class='ma-3 pa-6'
            outlined
            title>
              <v-img class="white--text" height="200px" src="../assets/image/starship-1.jpg"></v-img>

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

              <v-card-actions>
                <div class="text-right pl-0">
                  <div class="flex-grow-1"></div>
                  <!-- to remove shadow -->
                  <v-btn depressed dark color="black">Read More</v-btn>
                </div>
              </v-card-actions>
            </v-card>
          </v-row>
        </v-container>
        <!-- </v-col> -->
      </v-row>
    </div>
  </div>
</template>


<script>
export default {
  name: "StarshipCard",
  props: ["starships"]
};
</script>

<style scoped>
</style>
