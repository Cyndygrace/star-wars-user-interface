<template>
  <div>
    <div v-bind:key="character.id" v-for="character in characters">
      <v-row class="mx-auto ml-12">

        <v-card hover class="py-0 mb-12" max-height='390' max-width="600">
          
            <v-row>
              <v-img class="my-0 " width="100" height='390' src="../assets/image/character-1.jpg"></v-img>
            
            <v-col>
              <v-card-text class="pb-0">
                <p class="title font-weight-bold text--primary mb-0">Name: <br>{{character.name}}</p>
                <div class="mb-4">Year: {{character.birth_year}}</div>

                <div class="text--primary">Gender: {{character.gender}}</div>
              </v-card-text>
              <v-card-actions class="pt-0 pb-0">
                <v-btn text small class=" black--text">Read More</v-btn>
              </v-card-actions>
              <v-divider
                class=" ml-4 pt-1 black mt-0"
                style="opacity: 4"
                role="seperator"
                width="100"
                aria-orientation="horizontal"
              ></v-divider>
            </v-col>
          </v-row>
        </v-card>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  name: "CharacterCard",
  props: ["characters"]
};
</script>>