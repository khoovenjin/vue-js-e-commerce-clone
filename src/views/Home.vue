<template>
  <div class="splash-container">
    <div class="splash">
      <h1>Splendid Food</h1>
    </div>
  </div>

  <main class="wrapper">
    <h2>Recommended</h2>

    <div class="recommended">
      <ProductCard
        v-for="item in inventory.slice(0, 3)"
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
  name: 'Home',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
};
</script>
