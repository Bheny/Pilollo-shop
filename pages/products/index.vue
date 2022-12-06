<template>
  <div class="w-full pt-24 lg:pt-32">
    <section class="p-2 w-full border-l overflow-y-scroll h-screen">
      <div class="w-full">
        <div class="float-left lg:float-right gap-3 p-2 relative w-full">
          <button
            onclick="showContents('filterbox');"
            class="float-right border-black mx-2 rounded-full h-10 font-extrabold border-2 p-2 "
            >Filter By</button
          >
          <button
            onclick="openSortMenu();"
            class="float-right mx-2 border-black rounded-full h-10 font-extrabold border-2 p-2 focus:shadow-2xl"
          >
            Sort By
          </button>
          <div id="filter" class="hidden">
            <span
              onclick="openSortMenu();"
              class="hover:bg-gray-300 w-full block p-2 hover:bg-gray-300"
              >Highest Price</span
            >
            <span
              onclick="openSortMenu();"
              class="hover:bg-gray-300 w-full block p-2 hover:bg-gray-300"
              >Lowest Price</span
            >
            <span
              onclick="openSortMenu();"
              class="hover:bg-gray-300 w-full block p-2 hover:bg-gray-300"
              >Most Recent</span
            >
          </div>
        </div>
        <div class="float-right p-4"><!----></div>
      </div>
      <div
        class="grid gap-2 grid-cols-2 md:grid-cols-4 lg:grid-cols-6 p-2 w-full"
      >  
      <div v-for="product in products" v-bind:key="product">
          <ProductCard  :product="product"/>
        </div>
      </div>
      <div class="w-full text-center grid grid-cols-3">
        <div></div>
        <div class="p-2">
          <div class="w-full text-center flex"><div class="scroll">

          </div></div>
        </div>
        <div></div>
      </div>
    </section>
  </div>
</template>

<script setup>
const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>
