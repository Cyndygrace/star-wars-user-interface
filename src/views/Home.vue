<template>
  <div class="home">
    
  <Title v-bind:title='title1.text'/>
  <Title v-bind:title='title2.text'/>
  <Title v-bind:title='title3.text'/>

  </div>
</template>

<script>
import Title from '../components/Title'
export default {
name: 'Home',
components: {
Title
},
data() {
    return {
          title1: {text:'Popular Starship'},
          title2: {text:"Popular Planets"},
          title3: {text:"Popular Characters"},
      header: { text: "Things To Do" }
    };
  },
}
</script>