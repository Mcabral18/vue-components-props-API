<template>
  <section>
    <new-rocket-form class="container mt-5" :addRocket="addRocket" />
    <!-- passing array rocket to child compoent using props -->
    <rockets-list :rockets="rockets" :removeRocket="removeRocket" />
  </section>
</template>

<script>
import NewRocketForm from "../components/NewRocketForm.vue";
import RocketsList from "../components/RocketsList.vue";
// import api external file
import API from "../lib/API";
export default {
  components: {
    NewRocketForm,
    RocketsList,
  },
  data() {
    return {
      //array will store the api information
      rockets: [],
    };
  },
  // make api request on load
  async mounted() {
    this.rockets = await API.getRockets();
    console.log(this.rockets);
  },
  methods: {
    //this fuction push a rocket to the array rockets to be insert in the loop rocketList
    //them we pass this function as a prop to the newrocketform component to be used in that component
    addRocket(rocket) {
      this.rockets.push(rocket);
    },
    //we pass this method to the child rocket to be use there
    // We use a prop to pass a function
    removeRocket(rocket) {
      //remove from the array rockets a rocket and remove only 1 element
      this.rockets.splice(this.rockets.indexOf(rocket), 1);
      //*****************
      // const index = this.array.indexOf(elemento dentro do array);
      // this.array.splice(index, 1);
      //**** */ usage of the example *****
      //const index = this.rockets.indexOf(rocket);
      // this.rockets.splice(index, 1)
    },
  },
};
</script>

<style>
</style>