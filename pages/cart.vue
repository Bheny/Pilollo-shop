<template>
  <div class="pt-24">
    <div class="mb-8 pt-8 p-2 w-full relative">
      <div class="float-left absolute">Total(1 item)</div>
      <div class="float-right font-bold">GHC 95.00</div>
    </div>
    <section class="lg:flex lg:ml-32">
      <section class="lg:w-1/2">
        <div class="pt-0 border rounded m-2 bg-white">
          <!--cart -->
          <div class="border-b flex">
            <!-- body of cart -->

            <div class="p-0 h-32 w-32">
              <!-- image -->
              <img
                src="~/assets/stripes.jpg"
                class="rounded w-full h-full bg-center bg-contain"
                alt="item image"
              />
            </div>

            <div class="p-2">
              <!-- details -->
              <span class="text-sm font-bold">Ankara backpack </span>
              <div
                class="rounded-full h-6 pl-2 mt-1 bg-yellow-400 flex p-1 text-sm"
              >
                <img src="" class="w-4 h-4" /><span
                  class="text-xs"
                  >Pilollo tribe</span
                >
              </div>
              <span class="text-xs text-gray-600 block mt-1">Color: black</span>
              <span class="text-xs text-gray-600 block mt-1">Size: Small</span>
              <span class="text-md text-red-700 font-bold mb-2"
                >GHC 95.00
              </span>
            </div>
          </div>
          <div class="flex h-10">
            <!-- cart footer -->
            <!-- remove -->

            <div class="p-1 mt-1 w-2/5 flex">
              <button @click="quantity--" :disabled="(quantity<2)" class="border-2 rounded-lg font-bold">
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
              <input type="number" v-model="quantity" class="p-2 text-center w-10 text-xl" />
              <button @click="quantity++"  class="border-2 rounded-lg font-bold">
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
          </div>
          <!--div class="p-2 border-t">
				<div class="w-full">
				<div class="mb-2">
				<span class="text-sm font-bold hover:bg-gray-200 p-2 rounded-full block">Apply shop coupon codes</span>
			</div>
				<div class="mt-2 h-12 rounded-full flex border hidden">
					<input type="text" name="coupon" class="p-2 pl-4 w-4/6 rounded-l-full">
					<button class="float-right bg-red-700 text-white border font-bold rounded-r-full p-2 w-32">
						Apply
					</button>
				</div>
			</div>
			</div -->
        </div>
      </section>
      <div class="p-2 border rounded m-2 mb-6 bg-white h-34">
        <div class="mb-2 hidden">
          <div class="mt-4">
            <select
              name="delivery"
              class="border rounded shadow-lg p-2 bg-white w-full"
            >
              <option value="5">GHC 5.49 ( Standard Intracity )</option>
              <option value="20">GHC 19.49 ( Standard Intercity )</option>
            </select>
          </div>
          <div class="text-right p-2">
            <span class="text-gray-600 text-sm"
              >Ready to ship in 7-10 business days</span
            >
          </div>
        </div>
        <div>
          <span class="block font-bold mb-2">How you'll pay</span>
          <div class="p-2 mb-4 flex">
            <input type="radio" name="payment" class="bg-white" />
            <label class="ml-2 p-2 rounded border"
              ><img src="" class="rounded w-6 h-6"
            /></label>
          </div>
        </div>
        <div class="flex mb-2">
          <div class="w-2/5">
            <span class="">Total</span>
          </div>
          <div class="ml-6 text-right">
            <span class="text-red-700 font-bold block">GHC 95.00</span>
            <span class="text-gray-700 text-xs"
              >Delivery fees not included yet</span
            >
          </div>
        </div>

        <div class="flex w-full border">
          <button
            class="w-1/2 text-xs text-red-700 border border-red-800 p-1 rounded font-bold"
          >
            <a href="/Products/"> CONTINUE SHOPPING</a>
          </button>
          <a href="#login_to_continue" onclick="showContents('login');">
            <input type="text" value="next" hidden="" />
            <button
              class="w-full ml-2 text-xs text-white border bg-red-700 border-red-800 p-1 rounded font-bold pl-10 pr-10"
            >
              CHECKOUT
            </button></a
          >
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const quantity = ref(1);
</script>
