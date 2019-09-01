<template>
  <div>
    <!-- container -->
    <v-card app hover flat height="500" class="mx-auto">
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
<div class='text-center my-12 mb-0'>
        <span class="text-center display-1 font-weight-bold my-12">
          
          <img
            class="white--text text-center my-12 mb-0"
            height="50px"
            max-width="120"
            src="../assets/image/logo.png"
          />Directory
        </span>
</div>
        <!-- horizontal line -->
        <v-divider
          class="pt-1 mx-auto white mt-0"
          style="opacity: 4"
          role="seperator"
          width="300"
          aria-orientation="horizontal"
        ></v-divider>
      
        <v-card-text
          class="text-center mb-0 pb-0 title"
        >Find your favourite characters, films, species, starship and planets, Directory</v-card-text>
      
        <!-- earch input -->
        <v-form>
          <v-container height="200px" class="large">
            <v-row>
              <v-col cols="12" sm="6" class="mx-auto" >
                <v-text-field
                class='display-1 large'
                  height="60"
                  v-model="first"
                  prepend-inner-icon="mdi-magnify"
                  label="Search"
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

<script>
export default {
  name: "Header"
};
</script>>

<style scoped>
</style>>