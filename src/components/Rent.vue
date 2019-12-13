<template>
  <b-container>
    <b-row align-v="center">
      <house-card
        v-for="house in houses"
        :key="house.id"
        :name="house.name"
        :rating="house.rating"
        :image="house.image"
        :username="house.username"
        :status="house.status"
        :address="house.address"
        :price="house.price"
        :bedroom="house.bedroom"
        :bathroom="house.bathroom"
        :area="house.area"
      ></house-card>
    </b-row>
  </b-container>
</template>

<script>
import House from "../components/House.vue";

export default {
  name: "rent",
  components: {
    "house-card": House
  },
  data() {
    let houses = [
      {
        id: 1,
        name: "Patio Area At Home",
        rating: 2,
        image: require("../assets/house1.jpg"),
        username: "Cormac Finney",
        status: "Trust Real Estate",
        address: "7694 S. Fulton Road United States",
        price: 569,
        bedroom: 2,
        bathroom: 2,
        area: 420
      },
      {
        id: 2,
        name: "Old House",
        rating: 3,
        image: require("../assets/house2.jpg"),
        username: "Jaheim Gonzalez",
        status: "New User",
        address: "142 Riverside Lane United States",
        price: 980,
        bedroom: 1,
        bathroom: 1,
        area: 1100
      },
      {
        id: 3,
        name: "House At Lake",
        rating: 1,
        image: require("../assets/house3.jpg"),
        username: "Nial Rodriquez",
        status: "Trust Real Estate",
        address: "494 Border Rd. United States",
        price: 1530,
        bedroom: 2,
        bathroom: 2,
        area: 3500
      },
      {
        id: 4,
        name: "Old House",
        rating: 5,
        image: require("../assets/house4.jpg"),
        username: "Archie Brennan",
        status: "New User",
        address: "597 Glenholme St. United States",
        price: 990,
        bedroom: 1,
        bathroom: 1,
        area: 2010
      },
      {
        id: 5,
        name: "Near Beach House",
        rating: 3,
        image: require("../assets/house5.jpg"),
        username: "Theresa Case",
        status: "Trust Real Estate",
        address: "7654 Poplar St. United States",
        price: 1150,
        bedroom: 1,
        bathroom: 2,
        area: 1500
      },
      {
        id: 6,
        name: "House With Pool",
        rating: 4,
        image: require("../assets/house6.jpg"),
        username: "Halle Calhoun",
        status: "Trust Real Estate",
        address: "683 Miller Lane United States",
        price: 788,
        bedroom: 2,
        bathroom: 2,
        area: 1900
      }
    ];
    return {
      houses
    };
  }
};
</script>
