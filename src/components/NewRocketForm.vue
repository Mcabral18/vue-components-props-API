<template>
  <section>
    <button
      v-on:click="showForm = !showForm"
      type="button"
      class="btn btn-danger"
    >
      Show Form
    </button>
    <form v-if="showForm">
      <div class="form-group">
        <label for="Name">Name</label>
        <input
          type="text"
          class="form-control"
          name="name"
          id="name"
          value=""
        />
      </div>
      <!-- <div class="form-group">
        <label for="country">Country</label>
        <input
          type="text"
          class="form-control"
          name="country"
          id="country"
          value=""
        />
      </div> -->
      <div class="form-group">
        <label for="discription">Description</label>
        <input
          type="text"
          class="form-control"
          name="description"
          id="description"
          value=""
        />
      </div>
      <div class="form-group">
        <label for="image">Image</label>
        <input
          type="text"
          class="form-control"
          name="image"
          id="image"
          value=""
        />
      </div>
      <button class="btn btn-primary">Add Rocket</button>
    </form>
  </section>
</template>

<script>
export default {
  data() {
    return {
      showForm: false,
    };
  },
};
</script>

<style>
.btn {
  margin: 2rem 0;
}
</style>