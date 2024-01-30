<script setup>
import Card from "../components/Card.vue";
import {products} from "../data";
</script>

<template>
<section class="w-[1100px] mx-auto pt-[60px] px-[200px]">
  <div class="grid grid-cols-3 gap-[36px]">
    <Card
      v-for="(product, index) in products"
      :key="index"
      :topImg="product.topImg"
      :botImg="product.botImg"
      :mainImg="product.mainImg"
      :type="product.type"
      :name="product.name"
      :vendorСode="product.vendorСode"
      :price="product.price"
    />
  </div>
</section>
</template>
