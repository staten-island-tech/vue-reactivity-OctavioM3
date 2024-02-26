<template>
    <button class="prev" @click="prevcard">Previous Card</button>
    <div class="Cards">
        <h2>{{ CardsArray[CardNumber].name }}</h2>
        <p>{{ CardsArray[CardNumber].purchasecount.toLocaleString() }}</p>
        <p>Total Amount: ${{ (CardsArray[CardNumber].purchasecount * CardsArray[CardNumber].price).toLocaleString() }}</p>
    </div>
    <button class="next" @click="nextcard">Next Card</button>
    <div>
      <button class="confirm" @click="confirmpurchase">Confirm Purchase</button>
    </div>
</template>

<script setup>

import { ref } from 'vue';
import { clothes } from '@/stores/Clothing.js';

const props = defineProps({
  Clothes: Object,
});

const CardsArray = ref([...clothes]);
CardsArray.value.sort((a, b) => b.purchasecount - a.purchasecount);
const CardNumber = ref(0);

function prevcard() {
  CardNumber.value += -1;
  if (CardNumber.value < 0) {
        CardNumber.value = CardsArray.value.length - 1;
    }
  }

function nextcard() {
  CardNumber.value ++
  if (CardNumber.value > CardsArray.value.length - 1) {
        CardNumber.value = 0;
    }
}

function confirmpurchase() {

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
  background-color: black;
}
.prev {
width: 10vh;
margin-top: 3%;
margin-bottom: 1%;
}
.next {
  width: 10vh;
}

.confirm {
  margin-top: 50%;
}

</style>