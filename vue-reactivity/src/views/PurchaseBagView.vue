<template>
    <div class="PurchaseBag">
        <PurchaseCards
        />
    </div>
    <button class="PurchaseButton" @click="CompletePurchase">Complete Purchase</button>
        <h3><RouterLink :to="{ path: '/'}">Return To Shop</RouterLink></h3>
</template>

<script setup>
import PurchaseCards from '@/components/PurchaseCards.vue';

function CompletePurchase() {

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

</style>