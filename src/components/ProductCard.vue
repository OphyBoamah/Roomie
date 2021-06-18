<template>
  <div>
    <div class="w-80">
      <img :src="require(`../assets/img/${product.img}`)" :alt="product.name" class="w-full h-96"/>
      <div class="flex justify-between p-4">
        <h6>{{ product.name }}</h6>
        <p class="font-bold">{{ product.price }}</p>
      </div>
      <button class="bg-gray-800 text-white px-6 py-3 w-full font-bold">
        Add to cart</button>

    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props: ['product'],
};
</script>

<style scoped>

</style>
