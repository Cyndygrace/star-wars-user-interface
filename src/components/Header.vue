<template>
  <div>
    <!-- container -->
    <v-card hover flat height="500" class="mx-auto">
      <!-- image background -->
      <v-img class="white--text" height="640px" src="../assets/image/hero-banner.jpg">
        <!-- logo -->
        <v-img
          class="white--text ml-12 mt-8"
          height="50px"
          max-width="120"
          src="../assets/image/logo.png"
        ></v-img>
        <!-- logo beside text -->
        <v-card-text class="flex-grow-1 display-1 font-weight-bold text-center my-12 mb-0 pb-0">
          <v-img
            class="white--text mx-auto my-12 mb-0"
            height="50px"
            max-width="120"
            src="../assets/image/logo.png"
          ></v-img>Directory
        </v-card-text>
        <!-- horizontal line -->
        <v-divider
          class="success pt-1 mx-auto white mt-0"
          style="opacity: 4"
          role="seperator"
          width="300"
          aria-orientation="horizontal"
        ></v-divider>
        <v-card-text
          class="text-center mb-0 pb-0"
        >Find your favourite characters, films, species, starship and planets, Directory</v-card-text>
        <!-- earch input -->
        <v-form>
          <v-container height="200px">
            <v-row>
              <v-col cols="12" sm="6" class="mx-auto">
                <v-text-field
                  large
                  v-model="first"
                  prepend-inner-icon="mdi-magnify"
                  label="Search"
                  solo
                  height="24"
                >
                  <v-icon left>mdi-magnify</v-icon>
                </v-text-field>
              </v-col>
            </v-row>
          </v-container>
        </v-form>
      </v-img>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>>

<style scoped>
</style>>