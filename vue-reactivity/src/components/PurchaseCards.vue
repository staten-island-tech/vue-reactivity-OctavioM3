<template>
    <div class="Cards">
        <h2>{{ cardArray[cardIndex].name }}</h2>
        <p>{{ cardArray[cardIndex].purchasecount.toLocaleString() }}</p>
        <p>Total Amount: ${{ (cardArray[cardIndex].purchasecount * cardArray[cardIndex].price.toLocaleString) }}</p>
    </div>
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

</script>

<style scoped>

</style>