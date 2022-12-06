<template>
   <div>
      <NuxtLink :to="`/products/${product?.id}`">
        <div 
          class="item w-full lg:w-full bg-white rounded-lg shadow-lg mr-2 mb-2  inline-block"
        >
          <!-- Top card -->
          <div class="relative">
            <div class="h-48 ">
              <img
                  :src="product?.image"
                  class=" bg-current rounded-tl-lg rounded-tr-lg bg-transparent  h-full object-center object-contain"
                
              />
            </div>
            <div class="bg-transparent absolute text-center w-full top-0 my-1 mx-1">
              <!-- the like heart-->
              <div class="mr-2 pt-1 bg-white w-8 h-8 rounded-full float-right">
                <div>
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" :class="[]" class="mx-auto  w-6 h-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z" />
</svg>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="hidden w-5 h-5">
  <path d="M9.653 16.915l-.005-.003-.019-.01a20.759 20.759 0 01-1.162-.682 22.045 22.045 0 01-2.582-1.9C4.045 12.733 2 10.352 2 7.5a4.5 4.5 0 018-2.828A4.5 4.5 0 0118 7.5c0 2.852-2.044 5.233-3.885 6.82a22.049 22.049 0 01-3.744 2.582l-.019.01-.005.003h-.002a.739.739 0 01-.69.001l-.002-.001z" />
</svg>

                </div>
              </div>
            </div>
          </div>
          <!-- Bottom card -->

          <div class="p-2 bg-white">
            <a
              href="/Products/clothing-textiles/sports-wears/cardigans/99/ankara-bomber-jacket/ "
            >
              <span class="text-sm block truncate">  {{ product?.title }}</span></a
            >
            <span class="text-xs text-gray-600 block">Pilollo tribe</span>

            <span class="block flex text-xs">
              <span class=" flex text-red-700">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5">
  <path fill-rule="evenodd" d="M10.868 2.884c-.321-.772-1.415-.772-1.736 0l-1.83 4.401-4.753.381c-.833.067-1.171 1.107-.536 1.651l3.62 3.102-1.106 4.637c-.194.813.691 1.456 1.405 1.02L10 15.591l4.069 2.485c.713.436 1.598-.207 1.404-1.02l-1.106-4.637 3.62-3.102c.635-.544.297-1.584-.536-1.65l-4.752-.382-1.831-4.401z" clip-rule="evenodd" />
</svg> 

              </span>
              <i class="text-sm mt-1">{{product?.rating?.rate}} ({{product?.rating?.count}})</i>
            </span>

            <!-- div class="rounded-full h-6 pl-2 mt-1 bg-yellow-400 flex text-sm ">
                <img src="/static/img/store.png" class="mr-2"><span>Pilollo tribe</span>
              </div -->
            <span class="font-extrabold text-sm block inline-block"
              >GHC {{product?.price }}
            </span>
          </div>
        </div>
  
      </NuxtLink>
   </div> 
</template>

<script setup>
const { product } = defineProps(['product'])
</script>