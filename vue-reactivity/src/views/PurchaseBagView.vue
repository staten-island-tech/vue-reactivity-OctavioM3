<template>
    <div class="PurchaseBag">
        <PurchaseCards
        />
    </div>
        <h3><RouterLink :to="{ path: '/'}">Return To Shop</RouterLink></h3>
</template>

<script setup>
import PurchaseCards from '@/components/PurchaseCards.vue';
import { clothes } from '@/stores/Clothing.js'
</script>

<style scoped>

.PurchaseBag {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

</style>