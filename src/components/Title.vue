<template>
  <div>
        <div class='text-center my-12 mb-0'>
        <span class="text-center display-1 font-weight-bold my-12">
          {{title}}
        </span>
</div>
        <!-- horizontal line -->
        <v-divider
          class="info pt-1 mx-auto mt-2 white mt-0"
          style="opacity: 4"
          role="seperator"
          width="100"
          aria-orientation="horizontal"
          indigo
        ></v-divider>
    </div>
</template>


<script>
export default {
  name:'Title',
  props:['title'],
  data(){
    title: {
      text: text
    }
  }
}
</script>>

<style scoped>

</style>