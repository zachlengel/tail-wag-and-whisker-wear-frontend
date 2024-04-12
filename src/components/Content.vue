<script>
import OutfitsIndex from "./OutfitsIndex.vue";
import OutfitsNew from "./OutfitsNew.vue";

export default {
  components: {
    OutfitsIndex,
    PhotosNew,
  },
  data: function () {
    return {
      outfits: [
        { id: 1, name: "First", url: "https://via.placeholder.com/150", width: 150, height: 150 },
        { id: 2, name: "Second", url: "https://via.placeholder.com/300", width: 300, height: 300 },
      ],
    };
  },
  methods: {
    handleCreateOutfit: function (params) {
       axios
         .post("http://localhost:3000/outfits.json", params)
         .then((response) => {
           console.log("outfits create", response);
           this.outfits.push(response.data);
         })
         .catch((error) => {
           console.log("outfits create error", error.response);
         });
     },
  }
};
</script>

<template>
  <main>
    <OutfitsNew v-on:createOutfit="handleCreateOutfit"/>
    <OutfitsIndex v-bind:outfits="outfits" />
  </main>
</template>

<style></style>
