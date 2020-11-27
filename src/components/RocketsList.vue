<template>
  <section class="container">
    <div class="row">
      <rocket v-for="rocket in rockets" :key="rocket.id" :rocket="rocket" />
    </div>
  </section>
</template>

<script>
import Rocket from "./Rocket.vue";
export default {
  props: ["rockets"],
  components: {
    Rocket,
  },
};
</script>
