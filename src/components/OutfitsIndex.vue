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
      <img v-bind:src="outfit.url" />
      <p>Width: {{ outfit.width }}</p>
      <p>Height: {{ outfit.height }}</p>
    </div>
  </div>
</template>

<style></style>
