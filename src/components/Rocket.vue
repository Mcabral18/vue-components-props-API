<template>
  <div class="col-md-4">
    <div class="card" style="width: 18rem">
      <img :src="rocket.image" class="card-img-top" :alt="rocket.name" />
      <div class="card-body">
        <h5 class="card-title">
          {{ rocket.name }}
        </h5>
        <p class="card-text">
          {{ rocket.description.substring(0, 150) + "...." }}
        </p>
      </div>
      <button
        v-on:click="removeRocket(rocket)"
        type="button"
        class="btn btn-danger"
      >
        Delete Rocket
      </button>
    </div>
  </div>
</template>

<script>
export default {
  //props of the single rocket data that will repeat in the loop cicle component
  props: ["rocket", "removeRocket"],
};
</script>
