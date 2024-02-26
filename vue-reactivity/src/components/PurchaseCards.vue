<template>
    <button class="prev" @click="prevcard">Previous Card</button>
    <div class="Cards">
        <h2>{{ cardArray[cardIndex].name }}</h2>
        <p>{{ cardArray[cardIndex].purchasecount.toLocaleString() }}</p>
        <p>Total Amount: ${{ (cardArray[cardIndex].purchasecount * cardArray[cardIndex].price).toLocaleString() }}</p>
    </div>
    <button class="next" @click="nextcard">Next Card</button>
</template>

<script setup>

import { ref } from 'vue';
import { clothes } from '@/stores/Clothing.js';

const props = defineProps({
  Clothes: Object,
});

const cardArray = ref([...clothes]);
cardArray.value.sort((a, b) => b.purchasecount - a.purchasecount);
console.log(cardArray);
const cardIndex = ref(0);

function prevcard() {
  cardIndex.value += -1;
  if (cardIndex.value < 0) {
        cardIndex.value = cardArray.value.length - 1;
    }
  }

function nextcard() {
  cardIndex.value ++
  if (cardIndex.value > cardArray.value.length - 1) {
        cardIndex.value = 0;
    }
}

</script>

<style scoped>

.Cards {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin-bottom: 2vh;
  justify-content: space-evenly;
  border-radius: 5%;
  width: 30%;
  height: 100%;
  color: blanchedalmond;
  background-color: color;
}

</style>