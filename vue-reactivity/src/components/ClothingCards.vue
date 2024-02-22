<template>
  <div class="ClothesCard">
    <h1>{{ Clothes.name }}</h1>
    <img :src="Clothes.img" alt="" />
    <h2>{{ Clothes.color }}</h2>
    <h2> ${{ Clothes.price }}</h2>
    <button class="add" @click="addToBag">Purchase</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
  Clothes: Object,
});
</script>

<style scoped>
.ClothesCard {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  background-color: azure;
  margin-bottom: 2vh;
  justify-content: space-evenly;
  border-radius: 5%;
  width: 30%;
  height: 180%;
  color: blanchedalmond;
  background-color: black;
}


</style>