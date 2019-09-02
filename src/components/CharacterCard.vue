<template>
  <v-card
    class='ml-3 py-0'
    max-width="400"
  >
  <v-row>

  <v-col>
        <v-img
        class='my-0'
         height='100%'
          width="200"
          src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
        ></v-img>
      </v-col>
      <v-col>
    <v-card-text>
      <div>Word of the Day</div>
      <p class="display-1 text--primary">
        be•nev•o•lent
      </p>
      <p>adjective</p>
      <div class="text--primary">
        well meaning and kindly.<br>
        "a benevolent smile"
      </div>
    </v-card-text>
    <v-card-actions>
      <v-btn
        text
        color="deep-purple accent-4"
      >
        Learn More
      </v-btn>
    </v-card-actions>
    </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name:"CharacterCard"
}
</script>>