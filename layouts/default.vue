<template>
  <div class="w-full">
    <NewsletterModal :active="newsletter" />
    <ShoppingCart :active="onCart" />
    <header class="w-full fixed w-full bg-white shadow-lg z-20">
      <div class="flex gap-3 bg-black text-sm p-1 text-white">
        <h2 class="gap-2 flex">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="text-white w-4 h-4"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z"
            />
          </svg>
          (+233) 552274951
        </h2>
        <h2 class="gap-2  lg:inline-block flex">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="text-white w-4 inline h-4"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75"
            />
          </svg>
          info.pilollo@gmail.com
        </h2>
        <div id="top" class="mx-auto text-center">
        
        </div>
      </div>
      <nav class="w-full p-3 flex">
        <div class="text-center p-3 text-bold">
          <NuxtLink to="/"><img src="~/assets/Pilollo.png" class="-my-2 -mx-2 h-10 object-center object-contain" /></NuxtLink>
        </div>
        <div class="w-full flex">
          <div class="w-full inline bg-gray-100 rounded-lg h-10">
            <input
              type="text"
              class="inline p-2 rounded-lg bg-gray-100 w-4/5"
              placeholder="I am looking for ...."
            />
            <NuxtLink to="/products/"><svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="float-right mt-2 mr-2 w-6 h-6"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z"
              />
            </svg></NuxtLink>
          </div>
        </div>
        <div class="float-right flex">
          <button class="flex p-1 lg:p-3">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-6 h-6"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z"
              />
            </svg>
            <span class="hidden lg:inline-block ">Wishlist</span>
            
          </button>
          <NuxtLink to="/auth/login"><button class="flex p-1 lg:p-3">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-6 h-6"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M17.982 18.725A7.488 7.488 0 0012 15.75a7.488 7.488 0 00-5.982 2.975m11.963 0a9 9 0 10-11.963 0m11.963 0A8.966 8.966 0 0112 21a8.966 8.966 0 01-5.982-2.275M15 9.75a3 3 0 11-6 0 3 3 0 016 0z"
              />
            </svg>

            <span class="hidden lg:inline-block ">Account</span>
            
          </button></NuxtLink>
          <button @click="openCart()" class="flex p-1 lg:p-3 relative flex hover:border border-b-2 hover:border-black border-white">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-6 h-6"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M15.75 10.5V6a3.75 3.75 0 10-7.5 0v4.5m11.356-1.993l1.263 12c.07.665-.45 1.243-1.119 1.243H4.25a1.125 1.125 0 01-1.12-1.243l1.264-12A1.125 1.125 0 015.513 7.5h12.974c.576 0 1.059.435 1.119 1.007zM8.625 10.5a.375.375 0 11-.75 0 .375.375 0 01.75 0zm7.5 0a.375.375 0 11-.75 0 .375.375 0 01.75 0z"
              />
            </svg>
            <span class="mt-6 ml-2 text-center w-6 h-6 bg-gray-900 rounded-full text-white absolute top-0">0</span>

            <span class="hidden lg:inline-block ">Basket</span>

          </button>
        </div>
      </nav>
      <div class="hidden lg:inline-block w-full p-2">
        <ul class="flex text-sm gap-3">
          <li>All</li>
          <li v-for="category in categories" v-bind:key="category" class="flex gap-1">{{ category }} <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4 mt-1 ">
  <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
</svg>
</li>
        </ul>
      </div>
    </header>

    <!-- output the page content-->
    <div class="w-full">
      <slot />
    </div>
    <FooterComponent />
  </div>
</template>

<script setup>
const onCart = ref(false)
const newsletter = ref(null)

onMounted(() => {
  // localStorage.setItem('shoppingCart')
  setInterval(function() { newsletter.value=true},5000)
})

const openCart = () => {
  console.log("checking...",onCart.value)
  if(onCart.value == true){
    onCart.value=false
  }else{
    onCart.value=true
  }
}
let top = "timer starts here";
  const categories = ["Clothing & Textiles"]

  const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
  // Get today's date and time
  var current = new Date();

  var today = months[current.getMonth()] + " " + current.getDate() +" 2022 23:59:00";
// Set the date we're counting down to
var countDownDate = new Date(today).getTime();

// Update the count down every 1 second
// var x = setInterval(function() {

//   // Get today's date and time
//   var now = new Date().getTime();

//   // Find the distance between now and the count down date
//   var distance = countDownDate - now;

//   // Time calculations for days, hours, minutes and seconds
//   var days = Math.floor(distance / (1000 * 60 * 60 * 24));
//   var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
//   var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
//   var seconds = Math.floor((distance % (1000 * 60)) / 1000);
 
//   top= "Today's Deals Expire in " +  hours + "hrs "
//   + minutes + "min " + seconds + "sec ";

//   // If the count down is finished, write some text
 
//   if (distance < 0) {
//     clearInterval(x);

//     top = "EXPIRED";

//   }

// }, 1000);
</script>

