<template>
  <div class="StoreList">
    <ClothingCards
    v-for="clothing in clothes"
    :key="clothing.name"
    :Clothes="clothing"
    />
  </div>
</template>

<script setup>
import ClothingCards from '@/components/ClothingCards.vue';
const clothes = [
  {
    name: "Cargo Pants",
    color: "Black",
    price: 40,
    img: "insert img",
  },
  {
    name: "T-Shirt",
    color: "White",
    price: 20,
    img: "insert img",
  },
  {
    name: "Jeans",
    color: "Black",
    price: 30,
    img: "insert img",
  },
  {
    name: "T-Shirt",
    color: "Black",
    price: 20,
    img: "insert img",
  },
  {
    name: "Cargo Pants",
    color: "Cream",
    price: 40,
    img: "insert img",
  },
  {
    name: "Jeans",
    color: "Blue",
    price: 30,
    img: "insert img",
  },
  {
    name: "Hoodie",
    color: "White",
    price: 50,
    img: "insert img",
  },
  {
    name: "Hoodie",
    color: "Black",
    price: 50,
    img: "insert img",
  },
  {
    name: "Jacket",
    color: "Black",
    price: 80,
    img: "insert img",
  },
  {
    name: "Shorts",
    color: "Black",
    price: 20,
    img: "insert img",
  },
  {
    name: "Joggers",
    color: "Brown",
    price: 40,
    img: "insert img",
  },
  {
    name: "Joggers",
    color: "Black",
    price: 40,
    img: "insert img",
  },
];
</script>

<style  scoped>
.StoreList {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}


</style>