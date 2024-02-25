<template>
  <div class="ClothesCard">
    <h2>{{ Clothes.name }}</h2>
    <img :src="Clothes.img" alt="" />
    <p>{{ Clothes.color }}</p>
    <p> ${{ Clothes.price }}</p>
    <p>{{ Clothes.purchasecount }}</p>
    <button class="add" @click="addToBag">Purchase Item</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const props = defineProps({
  Clothes: Object,
});
const count = ref(props.Clothes.purchasecount);

function addToBag() {
  count.value++
}
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