<script>
import OutfitsIndex from "./OutfitsIndex.vue";
import OutfitsNew from "./OutfitsNew.vue";
import axios from "axios";

export default {
  components: {
    OutfitsIndex,
    OutfitsNew,
  },
  data: function () {
    return {
      outfits: [
        {
          id: 1,
          name: "Blonde Wig",
          url: "https://www.inspiremore.com/wp-content/uploads/2021/06/Dogs-wearing-wigs-1.jpg",
          price: "$19.99",
          description: "Make you dog feel like a star in this very fashionable wig.",
        },
        {
          id: 2,
          name: "Real Hair Wig",
          url: "https://m.media-amazon.com/images/I/61Oh2US5ZuL.jpg",
          price: "$99.99",
          description: "A wig made of real human hair to make your pet feel normal.",
        },
      ],
    };
  },
  methods: {
    handleCreateOutfit: function (params) {
      axios
        .post("http://127.0.0.1:5000/outfits.json", params)
        .then((response) => {
          console.log("outfits create", response);
          this.outfits.push(response.data);
        })
        .catch((error) => {
          console.log("outfits create error", error.response);
        });
    },
  },
};
</script>

<template>
  <main>
    <OutfitsNew v-on:createOutfit="handleCreateOutfit" />
    <OutfitsIndex v-bind:outfits="outfits" />
  </main>
</template>

<style></style>
