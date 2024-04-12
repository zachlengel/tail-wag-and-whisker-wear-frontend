<script>
export default {
  props: {
    outfits: Array,
  },
};
</script>

<template>
  <div>
    <h1>All outfits</h1>
    <div v-for="outfit in outfits" v-bind:key="outfit.id">
      <h2>{{ outfit.name }}</h2>
      <img v-bind:src="outfit.url" width="300px" height="300px" />
      <p>Price: {{ outfit.price }}</p>
      <p>Description: {{ outfit.description }}</p>
    </div>
  </div>
</template>

<style></style>
