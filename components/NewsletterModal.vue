<template>
  <div>
    <div
      id="popNewsletter"
      :class="[active ? 'block': 'hidden']"
      class="h-screen bg-black bg-opacity-75 z-30 pt-24 p-4 fixed w-full overflow-y-scroll"
    >
      <div
        class="border lg:mr-64 lg:ml-64 rounded-lg p-2 relative bg-yellow-300 opacity-100"
      >
        <div class="w-full bg-gray-100">
          <div
            @click="active=false"
            class="float-right pr-4"
          >
            <svg
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
              class="w-8 h-8 font-extrabold"
            >
              <path
                strokelinecap="round"
                strokelinejoin="round"
                strokewidth="{2}"
                d="M6 18L18 6M6 6l12 12"
              ></path>
            </svg>
          </div>
        </div>
        <div class="text-center p-4 lg:p-16">
          <h2 class="font-bold text-2xl text-black pt-12">
            WELCOME TO PILOLLO.
          </h2>
          <label class="font-bold text-xl text-gray-800"
            >Be the first to receive news on discounts, gift ideas, and
            incredible shopping offers</label
          ><br /><br />
          <div class="lg:pr-24 lg:pl-24">
            <input
              type="email"
              placeholder="example@gmail.com"
              required="required"
              class="p-2 border rounded-lg w-full"
            /><br /><br />
            <input
              type="text"
              placeholder="your phone Number"
              required="required"
              class="p-2 border rounded-lg w-full"
            /><br />
            <div class="w-full gap-4 lg:flex">
              <button
                class="border rounded-lg border-lg bg-red-700 text-white font-bold p-2 mt-2 w-full lg:w-1/2 inline"
              >
                i am a Male
              </button>
              <button
                class="border rounded-lg border-lg bg-red-700 text-white font-bold p-2 mt-2 w-full lg:w-1/2"
              >
                i am a Female
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const { active } = defineProps(['active'])
</script>
