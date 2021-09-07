<template>
  <li class="catalog__item">
    <a class="catalog__pic" href="#" @click.prevent="$emit('goToPage', 'product', {id: key})">
      <img :src="productImageLink" srcset="img/scooter@2x.jpg 2x" alt="Название товара">
    </a>

    <h3 class="catalog__title">
      <a href="#">
        {{ productLabel }}
      </a>
    </h3>

    <span class="catalog__price">
              {{ productPrice }} ₽
            </span>

    <ul class="colors colors--black">
      <li class="colors__item">
        <label class="colors__label" v-for="color in productColors" :key="color.id">
          <input class="colors__radio sr-only" type="radio" value="color.color">
          <span class="colors__value" :style="{'background-color': color.color}">
                  </span>
        </label>
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  props: ['productLabel', 'productPrice', 'productImageLink', 'productColors']
}
</script>