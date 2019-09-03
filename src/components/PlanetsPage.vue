<template>
  <div>
<v-row class="mx-auto ml-12">
      <v-col>
        <PlanetCard/>
      </v-col>
      <v-col>
        <PlanetCard />
      </v-col>
      <v-col>
        <PlanetCard />
      </v-col>
    </v-row>
  </div>
</template>>

<script>
import PlanetCard from '../components/PlanetCard'
export default {
  name: 'Planets',
  components:{
    PlanetCard
  },
  data(){
    return{
       planets: [
        {
          id: 1,
          image: "",
          title: "Corellia"
        },
        {
          id: 2,
          image: "",
          title: "Ord Mantel"
        },
        {
          id: 3,
          image: "",
          title: "Endor"
        }
      ],
      
    }
  }
}
</script>>