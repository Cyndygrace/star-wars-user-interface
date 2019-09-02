<template>
  <div>
    <div v-bind:key="character.id" v-for="character in characters">
      <v-row class="mx-auto ml-12">
        <v-card class="py-0" max-width="600">
          <v-row>
            <v-col>
              <v-img class="my-0" height="100%" width="350" src="../assets/image/character-1.jpg"></v-img>
            </v-col>
            <v-col>
              <v-card-text class="pb-0">
                <p class="display-1 text--primary mb-0">{{character.name}}</p>
                <div class="mb-4">{{character.title}}</div>

                <div class="text--primary">{{character.description}}</div>
              </v-card-text>
              <v-card-actions class="pt-0 pb-0">
                <v-btn text color="black accent-4">Read More</v-btn>
              </v-card-actions>
              <v-divider
                class="primary ml-5 pt-1 white mt-0"
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