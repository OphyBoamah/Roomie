<template>
  <header class="header relative pl-20" style="padding-top: 150px;">
  <h1 class="text-8xl font-black">Roomie</h1>
    <div class="header-text">
      <p>Article 1062</p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit.
        Amet blanditiis iste itaque natus necessitatibus praesentium
        quibusdam, quidem temporibus velit voluptatibus.
      </p>
      <form class="flex border-b border-gray-600 mt-10 pb-8">
        <input type="radio" id="male" name="gender" value="male">
        <label for="black">Black</label><br>
        <input type="radio" id="female" name="gender" value="female" class="ml-4">
        <label for="wood">Wood</label><br>
      </form>
      <button class="bg-gray-300 text-black p-5 font-bold mt-16">
        Add to your cart - $24
      </button>
    </div>
<!--    <div id="header-side" class="font-bold flex items-center justify-between px-6" >-->
<!--      <ul class="bg-white text-black flex p-4">-->
<!--        <li class="pr-4">fb</li>-->
<!--        <li class="pr-4">pi</li>-->
<!--        <li>in</li>-->
<!--      </ul>-->
<!--      <ul class="font-bold flex items-center justify-between text-black font-bold ">-->
<!--        <li class="pr-4">material</li>-->
<!--        <li class="pr-4">design</li>-->
<!--        <li class="pr-4">process</li>-->
<!--      </ul>-->
<!--    </div>-->

    <div class="font-bold flex items-center justify-between w-4/5 absolute transform"
              style="padding-top: 180px;" >
      <ul class="bg-white text-black flex p-4 w-40 justify-evenly items-center">
        <li>fb</li>
        <li>pi</li>
        <li>in</li>
      </ul>
      <ul class="flex w-80 justify-evenly items-center">
        <li>material</li>
        <li>design</li>
        <li>process</li>
      </ul>
    </div>
  </header>
  <main class="pt-96" style="padding-top: 900px;">
    <div class="flex justify-center">
      <div class="grid grid-cols-3 gap-10 ">
        <div v-for="product in products" :key="product.id">
          <ProductCard :product="product"/>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';

import ProductCard from '@/components/ProductCard.vue';

export default {
  name: 'Home',
  components: {
    ProductCard,
  },
  data() {
    return {
      products: [
        {
          id: 1,
          name: 'Product 1',
          price: '$590',
          img: '1.jpg',
        },
        {
          id: 2,
          name: 'Product 2',
          price: '$680',
          img: '2.jpg',
        },
        {
          id: 3,
          name: 'Product 3',
          price: '$240',
          img: '3.jpg',
        },
        {
          id: 4,
          name: 'Product 4',
          price: '$390',
          img: '4.jpg',
        },
        {
          id: 5,
          name: 'Product 5',
          price: '$150',
          img: '5.jpg',
        },
        {
          id: 6,
          name: 'Product 6',
          price: '$600',
          img: '6.jpg',
        },
        {
          id: 7,
          name: 'Product 7',
          price: '$370',
          img: '7.jpg',
        },
        {
          id: 8,
          name: 'Product 8',
          price: '$105',
          img: '8.jpg',
        },
        {
          id: 9,
          name: 'Product 9',
          price: '$500',
          img: '9.jpg',
        },
      ],
    };
  },
};
</script>
<style scoped>
.header {
  background-image: linear-gradient(rgba(0, 0, 0, .8), rgba(0, 0, 0, .8)),
      url("../assets/img/banner-2.jpg");
  background-position: center;
  background-size: cover;
  height: 100vh;
  position: absolute;
  inset: 0;
  text-align: left;
  color: #d4d4d8;
}

.header-text {
  width: 450px;
}
</style>
