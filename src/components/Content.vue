<script>
import OutfitsIndex from "./OutfitsIndex.vue";

export default {
  components: {
    OutfitsIndex,
  },
  data: function () {
    return {
      outfits: [
        { id: 1, name: "First", url: "https://via.placeholder.com/150", width: 150, height: 150 },
        { id: 2, name: "Second", url: "https://via.placeholder.com/300", width: 300, height: 300 },
      ],
    };
  },
};
</script>

<template>
  <main>
    <OutfitsIndex v-bind:outfits="outfits" />
  </main>
</template>

<style></style>
