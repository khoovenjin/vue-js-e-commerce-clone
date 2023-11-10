<template>
  <main class="wrapper">
    <h1>Products</h1>

    <div class="card-container">
      <ProductCard
        v-for="item in inventory.slice(0, 6)"
        :key="item.id"
        class="card"
        :item="item"
        :addToCart="addToCart"
      />
    </div>
  </main>
</template>

<script>
import ProductCard from '../components/ProductCard.vue';

export default {
  props: ['inventory', 'addToCart'],
  components: { ProductCard }
};
</script>
