<template>
  <section class="container">
    <div class="row">
      <!-- call the component rocket and create a loop for each rockt in rockets -->
      <!-- passing the props rocket, this means we only pass the data of a single rocket to the component -->
      <rocket
        v-for="(rocket, index) in rockets"
        :key="index"
        :rocket="rocket"
        :removeRocket="removeRocket"
      />
    </div>
  </section>
</template>

<script>
import Rocket from "./Rocket.vue";
export default {
  props: ["rockets", "removeRocket"],
  components: {
    Rocket,
  },
};
</script>
