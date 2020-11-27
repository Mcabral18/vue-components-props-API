<template>
  <section>
    <new-rocket-form class="container mt-5" />
    <rockets-list :rockets="rockets" />
  </section>
</template>

<script>
import NewRocketForm from "../components/NewRocketForm.vue";
import RocketsList from "../components/RocketsList.vue";
import API from "../lib/API";
export default {
  components: {
    NewRocketForm,
    RocketsList,
  },
  data() {
    return {
      rockets: [],
    };
  },
  // make api request
  async mounted() {
    this.rockets = await API.getRockets();
    console.log(this.rockets);
  },
};
</script>

<style>
</style>