<template>
  <div class="home">
    <Title v-bind:title="title1.text" />

    <StarshipCard v-bind:starships="starships" />

    <Title v-bind:title="title2.text" />
    <v-row class="mx-auto ml-12">
      <v-col>
        <PlanetCard v-bind:planets="planets" />
      </v-col>
      <v-col>
        <PlanetCard />
      </v-col>
      <v-col>
        <PlanetCard />
      </v-col>
    </v-row>

    <Title v-bind:title="title3.text" />

    <CharacterCard v-bind:characters="characters" />
  </div>
</template>

<script>
import Title from "../components/Title";
import CharacterCard from "../components/CharacterCard";
import StarshipCard from "../components/StarshipCard";
import PlanetCard from "../components/PlanetCard";
import axios from "axios";

export default {
  name: "Home",
  components: {
    Title,
    CharacterCard,
    StarshipCard,
    PlanetCard
  },
  data() {
    return {
      title1: { text: "Popular Starship" },
      title2: { text: "Popular Planets" },
      title3: { text: "Popular Characters" },
      starships: [
        // {
        //   id: 1,
        //   image: "",
        //   title: "Ghost",
        //   description:
        //     "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        // },
        // {
        //   id: 2,
        //   image: "",
        //   title: "Correllian Scout",
        //   description:
        //     "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        // },
        // {
        //   id: 3,
        //   image: "",
        //   title: "Raven's claw",
        //   description:
        //     "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        // },
        // {
        //   id: 4,
        //   image: "",
        //   title: "Loronar-E9 Explorer",
        //   description:
        //     "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        // },
        // {
        //   id: 5,
        //   image: "",
        //   title: "Raven's claw",
        //   description:
        //     "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        // },
        // {
        //   id: 6,
        //   image: "",
        //   title: "Outrider",
        //   description:
        //     "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        // }
      ],
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
      characters: [
        {
          id: 1,
          image: "",
          name: "Luke Skywalker",
          title: "Son of Anakin",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        },
        {
          id: 2,
          image: "",
          name: "Han Solo",
          title: "Cadet",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        },
        {
          id: 3,
          image: "",
          name: "Dart Varder",
          title: "Anakin Skywalker",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        },
        {
          id: 4,
          image: "",
          name: "Princess Leia",
          title: "Anakin Skywalker",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate similique fugiat aspernatur natus facilis aperiam tempora nostrum repudiandae placeat fuga"
        }
      ],
      header: { text: "Things To Do" }
    };
  },
  created() {
    axios
      .get("https://swapi.co/api/starships/?_limit=6")
      .then(res =>this.starships = res.data.results)
      .then(console.log(this.starships))
      .catch(error => console.log(error));
  }
};
</script>

