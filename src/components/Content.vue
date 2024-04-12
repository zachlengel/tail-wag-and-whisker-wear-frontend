<script>
import OutfitsIndex from "./OutfitsIndex.vue";

export default {
  components: {
    OutfitsIndex,
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
};
</script>

<template>
  <main>
    <OutfitsIndex v-bind:outfits="outfits" />
  </main>
</template>

<style></style>
