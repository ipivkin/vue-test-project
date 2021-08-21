<template>
  <li class="catalog__item">
    <a class="catalog__pic" href="#">
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
        <label class="colors__label">
          <input class="colors__radio sr-only" type="radio" name="color-6" value="#222" checked="">
          <span class="colors__value" style="background-color: #222;">
                  </span>
        </label>
      </li>
      <li class="colors__item">
        <label class="colors__label">
          <input class="colors__radio sr-only" type="radio" name="color-6" value="#73B6EA">
          <span class="colors__value" style="background-color: #73B6EA;">
                  </span>
        </label>
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  props: ['productLabel', 'productPrice', 'productImageLink']
}
</script>