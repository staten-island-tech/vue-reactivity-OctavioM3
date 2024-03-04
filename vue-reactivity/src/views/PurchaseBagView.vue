<template>
    <div class="PurchaseBag">
        <PurchaseCards
        />
    </div>
    <div class="PurchaseFeature">
    <button class="PurchaseButton" @click="CompletePurchase">Complete Purchase</button>
    <p class="TotalCost">Total Cost: ${{ totalCost }}</p>
    </div>
        <h3><RouterLink :to="{ path: '/'}">Return To Shop</RouterLink></h3>
</template>

<script setup>
import { ref } from 'vue';
import PurchaseCards from '@/components/PurchaseCards.vue';
import { clothes } from '@/stores/Clothing';

const totalCost = ref(0)

function CompletePurchase() {
  for (let clothe of clothes) {
    totalCost.value +=
    Number(clothe.purchasecount.value) *
    clothe.price;
  }
}
</script>

<style scoped>

.PurchaseBag {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
}
.PurchaseButton {
  text-align: center;
  align-items: center;
}
.PurchaseFeature{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
  margin-top: 5%;
}
.TotalCost {
  margin-top: 2%;
  font-size: 200%;
  margin-bottom: 2%;
  color: blanchedalmond;
}

</style>