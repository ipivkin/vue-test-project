
<template>
  <ul class="catalog__list">
      <ProductItem v-for="product in products" :key="product.id" :product-label="product.title" :product-price="product.price" :product-image-link="product.image"/>
  </ul>
</template>

<script>
import ProductItem from './ProductItem.vue'

export default {
  props: ['products'],
  components: { 
    ProductItem 
  }
}
</script>
