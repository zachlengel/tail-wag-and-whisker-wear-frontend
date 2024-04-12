<script>
export default {
  data: function () {
    return {
      newOutfitParams: {},
    };
  },
  methods: {
    handleSubmit: function () {
      this.$emit("createOutfit", this.newOutfitParams);
      this.newOutfitParams = {};
    },
  },
};
</script>

<template>
  <div id="newoutfits">
    <h1>New Posting</h1>
    <form>
      <div>
        Name:
        <input type="text" v-model="newOutfitParams.name" />
      </div>
      <div>
        Animal_id:
        <input type="integer" v-model="newOutfitParams.animal_id" />
      </div>
      <div>
        Price:
        <input type="decimal" v-model="newOutfitParams.price" />
      </div>
      <div>
        Url:
        <input type="text" v-model="newOutfitParams.url" />
      </div>
      <button type="submit">Create posting</button>
    </form>
  </div>
</template>

<style></style>
