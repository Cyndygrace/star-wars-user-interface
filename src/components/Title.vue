<template>
  <div>
        <div class='text-center my-12 mb-0'>
        <span class="text-center headline font-weight-bold my-12">
          {{title}}
        </span>
</div>
        <!-- horizontal line -->
        <v-divider
          class="black pt-1 mx-auto mt-2 mt-0 mb-4"
          style="opacity: 4"
          role="seperator"
          width="100"
          aria-orientation="horizontal"
        ></v-divider>
    </div>
</template>


<script>
export default {
  name:'Title',
  props:['title'],
  }

</script>>

<style scoped>

</style>