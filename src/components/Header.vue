<template>
  <div>
    <!-- container -->
    <v-card hover flat height="550" class="mx-auto">
      <!-- image background -->
      <v-img class="white--text" height="550px" src="../assets/image/hero-banner.jpg">
        <!-- logo -->
        <v-img
          class="white--text ml-4 mt-4"
          height="50px"
          max-width="120"
          src="../assets/image/logo.png"
        ></v-img>
        <!-- logo beside text -->
        <div class="text-center my-12 mb-0">
          <span class="text-center display-1 font-weight-bold my-12 mb-12">
            <img
              class="white--text text-center my-8 mb-0 mr-4"
              height="50px"
              src="../assets/image/logo.png"
            />Directory
          </span>
        </div>
        <!-- horizontal line -->
        <v-divider
          class="pt-1 mx-auto white mt-0 mt-2 mb-2"
          style="opacity: 4"
          role="seperator"
          width="300"
          aria-orientation="horizontal"
        ></v-divider>

        <v-card-text class="text-center mb-2 pb-0 title">
          Find your favourite characters, films, species,
          <br />starship and planets, Directory
        </v-card-text>

        <!-- earch input -->
        <v-form @submit="submit">
          <v-container>
            <v-row>
              <v-col cols="12" sm="8" class="mx-auto">
                <v-text-field
                  class="display-1 font-size-30"
                  height="70"
                  v-model="search"
                  prepend-inner-icon="mdi-magnify"
                  label="Enter a search term"
                  solo
                >
                  <!-- <v-icon left large>mdi-magnify</v-icon> -->
                </v-text-field>
              </v-col>
            </v-row>
          </v-container>
        </v-form>
      </v-img>
    </v-card>
  </div>
</template>
<style scoped>
.v-icon {
  font-size: 44px !important;
}
.v-input input::-webkit-input-placeholder {
  font-size: 5rem !important;
}
</style>
<script>
export default {
  name: "Header",
  data() {
    return {
      search: ""
    };
  },
  methods: {
    submit() {
      console.log(this.search);
    }
  }
};
</script>