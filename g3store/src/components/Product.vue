<template>
  <div class="card_container">
    <div class="card_image">
      <img :src="API_URL + product.Image.url" alt="{{product.Name}}" />
    </div>
    <div class="card_title">{{ product.Name }}</div>
    <div class="card_text">
      <p>{{ product.Description }}</p>
    </div>
    <div class="card_footer">
      <div class="card_price">{{ product.Price }}</div>
      <div>
        <button class="btn btn-primary btn-sm">Agregar</button>
      </div>
    </div>
  </div>
</template>

<script>
import { API_URL } from '../utils/constants';
export default {
  name: 'Product',
  props: {
    product: Object,
    title: String
  },

  setup() {
    return {
      API_URL,
    };
  },
};
</script>

<style></style>
