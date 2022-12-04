<template>
  <div class="w-full border pt-24 lg:pt-32">
    <div class="w-full text-white bg-[#5e0303] mt-3 overflow-x-scroll">
      <ul class="flex text-sm font-bold gap-6">
        <li class="hover:bg-black hover:text-white rounded-lg p-3">
          Best Deals
        </li>
        <li class="hover:bg-black hover:text-white rounded-lg p-3">
          Flash Sales
        </li>
        <li class="hover:bg-black hover:text-white rounded-lg p-3">
          Best Sellers
        </li>
        <li class="hover:bg-black hover:text-white rounded-lg p-3">
          Editor's Choice
        </li>
        <li class="hover:bg-black hover:text-white rounded-lg p-3">About Us</li>
      </ul>
    </div>
    <div class="bg-gray-700 p-2">
      <h2 class="text-white font-bold text-lg text-center">
        Find the perfect African Inspired Gift and More with Pilollo Tribe
      </h2>
      <div class="w-full grid grid-cols-3 lg:grid-cols-6 gap-1 lg:gap-3 py-6">
        <div
          v-for="category in 6"
          v-bind:key="category"
          class="p-3 text-center mx-auto"
        >
          <div class="rounded-full">
            <img
              src="~/assets/ella.jpg"
              class="rounded-full w-24 lg:w-32 h-24 lg:h-32 mx-auto"
            />
          </div>
          <h2 class="text-white">Party Freak</h2>
        </div>
      </div>
    </div>
    <div class="deals mt-3 pt-4 rounded-lg w-full">
      <div class="my-12 border rounded-lg bg-white mt-3">
        <div class="p-3">
          <h2 class="text-slate-600 text-lg">Deals Of The Day</h2>
          <h1 id="demo" class="text-xl text-red-700 font-bold">{{ timer }}</h1>
        </div>
        <div class="w-full grid grid-cols-2 lg:grid-cols-0 mt-3">
          <DealProductCard />
        </div>
      </div>
    </div>
    <div class="scroll w-full lg:grid lg:grid-cols-5">
      <div class="item w-full lg:w-64 text-center mb-8 p-4">
        <div class="text-center w-full">
          <div class="w-8 h-8 text-center mx-auto">
            <svg
              classname="mx-auto w-6 h-6"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                strokelinecap="round"
                strokelinejoin="round"
                strokewidth="{2}"
                d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"
              ></path>
            </svg>
          </div>
        </div>
        <div class="w-full">
          <span class="block font-semibold">23/7 dedicated service</span>
          <span class="block text-sm"
            >Experience our unrivaled customer service.</span
          >
          <span class="lg:hidden font-bold italic">swipe -&gt;</span>
        </div>
      </div>
      <div class="item w-full lg:w-64 text-center mb-8 p-4">
        <div class="text-center w-full">
          <div class="mx-auto w-8 h-8 text-center">
            <svg
              classname="mx-auto w-6 h-6"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                strokelinecap="round"
                strokelinejoin="round"
                strokewidth="{2}"
                d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"
              ></path>
            </svg>
          </div>
        </div>
        <div class="w-full">
          <span class="block font-semibold">Secure Shopping</span>
          <span class="block text-sm">All your information are secured</span>
          <span class="lg:hidden font-bold italic">swipe -&gt;</span>
        </div>
      </div>
      <div class="item w-full lg:w-64 text-center mb-8 p-4">
        <div class="text-center w-full">
          <div class="mx-auto w-8 h-8 text-center">
            <svg
              classname="w-6 h-6"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M9 17a2 2 0 11-4 0 2 2 0 014 0zM19 17a2 2 0 11-4 0 2 2 0 014 0z"
              ></path>
              <path
                strokelinecap="round"
                strokelinejoin="round"
                strokewidth="{2}"
                d="M13 16V6a1 1 0 00-1-1H4a1 1 0 00-1 1v10a1 1 0 001 1h1m8-1a1 1 0 01-1 1H9m4-1V8a1 1 0 011-1h2.586a1 1 0 01.707.293l3.414 3.414a1 1 0 01.293.707V16a1 1 0 01-1 1h-1m-6-1a1 1 0 001 1h1M5 17a2 2 0 104 0m-4 0a2 2 0 114 0m6 0a2 2 0 104 0m-4 0a2 2 0 114 0"
              ></path>
            </svg>
          </div>
        </div>
        <div class="w-full">
          <span class="block font-semibold">Fast delivery</span>
          <span class="block text-sm"
            >Quick and timely delivery of all your Orders</span
          >
          <span class="lg:hidden font-bold italic">swipe -&gt;</span>
        </div>
      </div>
      <div class="item w-full lg:w-64 text-center mb-8 p-4">
        <div class="text-center w-full">
          <div class="mx-auto w-8 h-8 text-center">
            <svg
              class="w-6 h-6"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                strokelinecap="round"
                strokelinejoin="round"
                strokewidth="{2}"
                d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"
              ></path>
            </svg>
          </div>
        </div>
        <div class="w-full">
          <span class="block font-semibold">Verified Sellers</span>
          <span class="block text-sm"
            >Meet Every day people selling items they love .</span
          >
          <span class="lg:hidden font-bold italic">swipe -&gt;</span>
        </div>
      </div>
      <div class="item w-full lg:w-64 text-center text-gray-700 mb-8 p-4">
        <div class="text-center w-full">
          <div class="mx-auto w-8 h-8 flex text-center">
            <svg
              class="w-6 h-6"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                strokelinecap="round"
                strokelinejoin="round"
                strokewidth="{2}"
                d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"
              ></path>
            </svg>
          </div>
        </div>
        <div class="w-full mt-2">
          <span class="block font-semibold"> 30 Days Return </span>
          <span class="block text-sm"
            >We garantee to you a 30 days return on goods
          </span>
        </div>
      </div>
    </div>
    <section class="w-full">
      <div id="app2" class="rounded-lg bg-yellow-400 p-4 text-center">
        <div class="w-full">
          <span class="text-gray-900 text-lg block">
            Hey , CHECK THIS OUT !!</span
          >
          <span class="text-gray-800 font-extrabold text-xl mb-2"
            >Be the first to recieve news on discounts, gift ideas, and
            incredible shopping offers</span
          >
        </div>
        <div class="w-full text-center p-4">
          <button
            type="button"
            class="bg-black text-white text-center hover:bg-white hover:text-yellow-500 font-extrabold p-2 rounded-full h-12 pl-8 pr-8"
          >
            Yes, sign me up
          </button>
        </div>
      </div>
    </section>
    <section id="bestsellers" class="p-2 mt-6 ">
      <div class="w-full p-4 text-left">
        <h2 class="text-xl font-extrabold">Top Sellers</h2>
      </div>
      <div
        class="grid gap-2 grid-cols-2 md:grid-cols-4 p-2 lg:grid-cols-7 lg:gap-2"
      >
        <div v-for="product in products" v-bind:key="product">
          <ProductCard :product="product"/>
        </div>
        
      </div>
    </section>
    <section class="bg-gray-100">
      <div class="w-full p-4 text-left lg:flex">
        <div class="inline-block">
          <h2 class="text-xl font-extrabold text-gray-700">New Arrivals</h2>
        </div>
        <div class="float-right">
          <a href="/Products/"
            ><span class="text-gray-900 ml-12 mt-1">See more</span></a
          >
        </div>
      </div>
      <div
        class="grid gap-2 grid-cols-2 md:grid-cols-4 p-2 lg:grid-cols-7 lg:gap-2"
      >
        <ProductCard :products="6" />
      </div>
    </section>

    <section v-for="(category,index) in categories" v-bind:key="category" :class="[ (index%2) == 0 ? 'bg-white':'bg-gray-100' ]" class="p-2 mt-6 ">
      <div class="w-full p-4 text-left lg:flex">
        <div class="inline-block">
          <h2 class="text-xl font-extrabold">
            {{ category }} 
          </h2>
        </div>
        <div class="float-right">
          <a href="/Products/clothing-textiles/"
            ><span class="text-gray-900 ml-12 mt-1">See more</span></a
          >
        </div>
      </div>
      <div
        class="grid gap-2 grid-cols-2 md:grid-cols-4 p-2 lg:grid-cols-7 lg:gap-2"
      >
      <div v-for="product in products" v-bind:key="product">
          <ProductCard v-if="(product.category == category)" :product="product"/>
        </div>
      </div>
    </section>

    <section :class="[(categories.length%2) == 0 ? 'bg-white ':' bg-gray-100' ]" class="p-2 mt-6 ">
      <div class="w-full p-4 text-left lg:flex">
        <h2 class="text-xl font-extrabold inline-block">Most Viewed</h2>
        <div class="float-right">
          <a href="/Products/Most_Viewed/"
            ><span class="text-gray-900 ml-12 mt-1">See more</span></a
          >
        </div>
        <div
          class="grid gap-2 grid-cols-2 md:grid-cols-4 p-2 lg:grid-cols-7 lg:gap-2"
        >
          <ProductCard :products="6" />
        </div>
      </div>
    </section>

    <section>
      <div :class="[(categories.length%2) == 0 ? 'bg-gray-100':' bg-white' ]" class="w-full p-4 text-left lg:flex">
        <div class="inline-block">
          <h2 class="text-xl font-extrabold">Shop Our Picks</h2>
        </div>
        <div class="float-right">
          <a href="/Products/clothing-textiles/"
            ><span class="text-gray-900 ml-12 mt-1">See more</span></a
          >
        </div>
        <div
          class="grid gap-2 grid-cols-2 md:grid-cols-4 p-2 lg:grid-cols-7 lg:gap-2"
        >
          <ProductCard :products="6" />
        </div>
      </div>
    </section>
    <section>
      <div
        id="item"
        class="grid gap-2 grid-cols-2 md:grid-cols-4 p-2 lg:grid-cols-6 lg:gap-4"
      >
        <div
          v-for="catalog in catalogues"
          v-bind:key="catalog"
          class="rounded-lg bg-white hover:animate-pulse ease-linear duration-300 mb-2"
        >
          <!-- Top card -->
          <div class="relative">
            <div class="h-48">
              <a href="/Products/Gifts/anniversary/"
                ><img
                  src="~/assets/stripes.jpg"
                  class="w-full h-full object-cover object-center rounded-tl-lg rounded-tr-lg bg-gray-300"
              /></a>
            </div>
            <div
              class="hidden absolute text-center w-full top-0 my-1 mx-1"
            ></div>
          </div>

          <div class="p-2 text-center font-bold">
            <a href="">
              <span class="text-sm block"> {{ catalog }}</span></a
            >
          </div>
          <div></div>
        </div>
      </div>
    </section>
    <section class="lg:flex w-full grid lg:grid-cols-4">
      <div class="h-full bg-yellow-400 p-4 w-full lg:col-span-2">
        <div class="p-4 w-full lg:pl-32">
          <h1 class="text-6xl">
            WHAT<br />
            PEOPLE <br />SAY <br />ABOUT<br />
            US
          </h1>
        </div>
      </div>
      <div class="border-b lg:col-span-2 lg:pt-24">
        <div class="text-center p-4 relative">
          <span class="font-extrabold text-3xl text-gray-800 block"
            >TESTIMONIES</span
          >
          <span class="text-sm font-extrabold text-gray-600"
            >What people say about us</span
          >
        </div>
        <div class="">
          <div class="w-full flex">
            <!-- Card section -->
            <div class="">
              <!-- card -->
              <div class="w-full h-24 mb-2 text-center">
                <!-- card head -->

                <img
                  src="~/assets/ella.jpg"
                  class="mx-auto rounded-full h-24 w-24 bg-cover"
                />
              </div>

              <div class="text-center">
                <!-- card bottom -->
                <span class="font-extrabold text-lg block">Clement</span>
                <span class="text-gray-800 mb-2">Customer</span>

                <hr class="w-12 mx-auto mt-2" />

                <div class="text-gray-600 p-4">
                  <p>
                    Surely there are a lot of african marketplaces in the space
                    but This site has taken it to another level, the fun and
                    experience leaves a lingering effect. Sometimes i want to
                    just buy from them for no reason . Kudos guys.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
// v-if="product.category.includes('clothing','jewelery')"
// const categories = [
//   "Clothing & Textiles",
//   "Foot wears",
//   "Jewelry & Accesories",
//   "Custome Arts & Craft"
// ];
const { data: categories }= await useFetch('https://fakestoreapi.com/products/categories')
const catalogues = [
  "Anniversary",
  "Gifts For Him",
  "Custom Boxes",
  "Gifts For Her",
];
const { data: products } = await useFetch('https://fakestoreapi.com/products')
var timer = "loading";
let vm = this;
const months = [
  "January",
  "February",
  "March",
  "April",
  "May",
  "June",
  "July",
  "August",
  "September",
  "October",
  "November",
  "December",
];
// Get today's date and time
var current = new Date();

var today =
  months[current.getMonth()] + " " + current.getDate() + " 2022 23:59:00";
// Set the date we're counting down to
var countDownDate = new Date(today).getTime();

// Update the count down every 1 second
// var x = setInterval(function () {
//   // Get today's date and time
//   var now = new Date().getTime();

//   // Find the distance between now and the count down date
//   var distance = countDownDate - now;

//   // Time calculations for days, hours, minutes and seconds
//   var days = Math.floor(distance / (1000 * 60 * 60 * 24));
//   var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
//   var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
//   var seconds = Math.floor((distance % (1000 * 60)) / 1000);

//   // Display the result in the element with id="demo"

//   timer = hours + "hrs " + minutes + "min " + seconds + "sec ";

//   // If the count down is finished, write some text

//   if (distance < 0) {
//     clearInterval(x);

//     timer = "EXPIRED";
//   }
// }, 1000);
</script>

<style scoped>
.deals {
  background-image: url("stripes.jpg");
}
</style>
