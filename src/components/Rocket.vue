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
    </div>
  </div>
</template>

<script>
export default {
  props: ["rocket"],
};
</script>
