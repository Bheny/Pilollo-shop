<template>
  <div
    :class="[active ? 'block' : 'hidden']"
    class="fixed z-30 bg-black bg-opacity-50 h-screen w-full"
  >
    <div class="relative bg-white h-screen float-right w-full lg:w-1/4">
      <div class=" bg-gray-800 p-3 py-4 ">
        <h2 class=" text-gray-100 w-1/2 inline ">My Basket</h2>
        <svg @click="(active=false)" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="font-bold text-gray-100 inline float-right w-6 h-6">
  <path fill-rule="evenodd" d="M5.47 5.47a.75.75 0 011.06 0L12 10.94l5.47-5.47a.75.75 0 111.06 1.06L13.06 12l5.47 5.47a.75.75 0 11-1.06 1.06L12 13.06l-5.47 5.47a.75.75 0 01-1.06-1.06L10.94 12 5.47 6.53a.75.75 0 010-1.06z" clip-rule="evenodd" />
</svg>

      </div>
      <div class="mb-8 pt-8 p-2 w-full ">
        <div class="float-left absolute">Total(1 item)</div>
        <div class="float-right font-bold">GHC 95.00</div>
      </div>
      <section class="w-full h-screen overflow-y-scroll">
        <div
          v-for="item in 12"
          @key="item"
          class="pt-0 border rounded m-2 bg-white"
        >
          <!--cart -->
          <div class="border-b flex">
            <!-- body of cart -->

            <div class="p-0 h-16 w-16">
              <!-- image -->
              <img
                src="~/assets/stripes.jpg"
                class="rounded w-full h-full bg-center bg-contain"
                alt="item image"
              />
            </div>

            <div class="p-2">
              <!-- details -->
              <span class="text-sm font-bold">Ankara backpack </span><br />
              <span class="text-md w-full text-red-700 font-bold mb-2"
                >GHC 95.00
              </span>
              <!-- <span class="text-xs text-gray-600 block mt-1">Color: black</span>
              <span class="text-xs text-gray-600 block mt-1">Size: Small</span> -->
            </div>
            <div class="pt-6 text-right">
              
            </div>
          </div>
          <div class="flex h-10">
            <!-- cart footer -->
            <!-- remove -->

            <div class="p-1 mt-1 w-1/2 flex">
              <button
                @click="quantity--"
                :disabled="quantity < 2"
                class="border-2 rounded-lg font-bold"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 24 24"
                  fill="currentColor"
                  class="w-6 h-6"
                >
                  <path
                    fill-rule="evenodd"
                    d="M3.75 12a.75.75 0 01.75-.75h15a.75.75 0 010 1.5h-15a.75.75 0 01-.75-.75z"
                    clip-rule="evenodd"
                  />
                </svg>
              </button>
              <input
                type="number"
                v-model="quantity"
                class="p-2 text-center w-10 text-xl"
              />
              <button @click="quantity++" class="border-2 rounded-lg font-bold">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 24 24"
                  fill="currentColor"
                  class="w-6 h-6"
                >
                  <path
                    fill-rule="evenodd"
                    d="M12 3.75a.75.75 0 01.75.75v6.75h6.75a.75.75 0 010 1.5h-6.75v6.75a.75.75 0 01-1.5 0v-6.75H4.5a.75.75 0 010-1.5h6.75V4.5a.75.75 0 01.75-.75z"
                    clip-rule="evenodd"
                  />
                </svg>
              </button>
            </div>
            <div class="pt-2  w-1/2 pr-2">
              <!-- <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class=" w-6 h-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M14.74 9l-.346 9m-4.788 0L9.26 9m9.968-3.21c.342.052.682.107 1.022.166m-1.022-.165L18.16 19.673a2.25 2.25 0 01-2.244 2.077H8.084a2.25 2.25 0 01-2.244-2.077L4.772 5.79m14.456 0a48.108 48.108 0 00-3.478-.397m-12 .562c.34-.059.68-.114 1.022-.165m0 0a48.11 48.11 0 013.478-.397m7.5 0v-.916c0-1.18-.91-2.164-2.09-2.201a51.964 51.964 0 00-3.32 0c-1.18.037-2.09 1.022-2.09 2.201v.916m7.5 0a48.667 48.667 0 00-7.5 0" />
</svg> -->
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="float-right text-red-700 w-6 h-6"
              >
                <path
                  fill-rule="evenodd"
                  d="M16.5 4.478v.227a48.816 48.816 0 013.878.512.75.75 0 11-.256 1.478l-.209-.035-1.005 13.07a3 3 0 01-2.991 2.77H8.084a3 3 0 01-2.991-2.77L4.087 6.66l-.209.035a.75.75 0 01-.256-1.478A48.567 48.567 0 017.5 4.705v-.227c0-1.564 1.213-2.9 2.816-2.951a52.662 52.662 0 013.369 0c1.603.051 2.815 1.387 2.815 2.951zm-6.136-1.452a51.196 51.196 0 013.273 0C14.39 3.05 15 3.684 15 4.478v.113a49.488 49.488 0 00-6 0v-.113c0-.794.609-1.428 1.364-1.452zm-.355 5.945a.75.75 0 10-1.5.058l.347 9a.75.75 0 101.499-.058l-.346-9zm5.48.058a.75.75 0 10-1.498-.058l-.347 9a.75.75 0 001.5.058l.345-9z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>
          </div>
        </div>
      </section>
      <div class="absolute bottom-0 pb-24 flex w-full border bg-white pt-4 p-2">
        <button
          class="py-3 w-1/2 text-xs text-red-700 border border-red-800 p-1 rounded font-bold"
        >
          <a href="/Products/"> CONTINUE SHOPPING</a>
        </button>

          <button
            class="py-3 w-full ml-2 text-xs text-white border bg-yellow-500 border-red-800 p-1 rounded font-bold pl-10 pr-10"
          >
            CHECKOUT
          </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const quantity = ref(1);
let shoppingCart = ref([]);
const { active } = defineProps(["active"]);
</script>
