<template>

  <div class="StoreList">
    <ClothingCards
    v-for="clothing in clothes"
    :key="clothing.name"
    :Clothes="clothing"
    />
  </div>
  <h3><RouterLink :to="{ path: '/bag'}">Go to Bag</RouterLink></h3>
</template>

<script setup>
import ClothingCards from '@/components/ClothingCards.vue';
import { clothes } from '@/stores/Clothing.js';
</script>

<style scoped>
.StoreList {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}


</style>