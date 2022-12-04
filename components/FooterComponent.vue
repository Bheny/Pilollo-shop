<template>
    <div>
        
      <section class="text-center">

<a href="#main">
  <button class="h-12 w-full bg-red-900 text-sm text-white" style="background-color: #7b0a0a;">TOP OF PAGE</button>
</a>
</section>
<section class="footerBg p-2 bg-cover" >
      <div class="p-2 lg:flex">
        <div class="w-full text-white">
          <div class="w-full h-8 p-1 text-white block hover:bg-red-400" onclick="show('knowus');">
            <div class="float-left font-bold block">
                Know Us
            </div>
            <div class="float-right lg:hidden">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
            </div>
          </div>
             <!-- dropdown for know us -->
           <div id="knowus" class="hidden lg:block">
               <span class="block p-2 hover:underline">Pilollo Tribe, Ltd</span>
                <a href="/about/"><span class="block p-2 hover:underline">Our unique story</span></a>
                <a href="/Privacy_Policy/"><span class="block p-2 hover:underline">Privacy Policy</span></a>
               <a href="/Terms-and-conditions/"><span class="block p-2 hover:underline">Terms and conditions</span></a>
               <span class="block p-2 hover:underline">Blog</span>
               <span class="block p-2 hover:underline">Impact</span>

           </div>
           </div>
        <div class="w-full text-white">
          <div class="w-full h-8 p-1 text-white block hover:bg-red-400" onclick="show('sell');">
            <div class="float-left font-bold block">
                Make Money
            </div>
            <div class="float-right lg:hidden">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
            </div>
          </div>
             <!-- dropdown for make money -->
           <div id="sell" class="hidden lg:block">
               <span class="block p-2 hover:underline">sell on Pilollo</span>
               <a href="/Seller-Terms-and-conditions/"><span class="block p-2 hover:underline">seller terms</span></a>
               <span class="block p-2 hover:underline">Affiliates</span>
           </div>
           </div>

           <div class="w-full text-white">
          <div class="w-full h-8 p-1 text-white block hover:bg-red-400" onclick="show('shop');">
            <div class="float-left font-bold block">
                Shop
            </div>
            <div class="float-right lg:hidden">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
            </div>
          </div>
             <!-- dropdown for Shop-->
           <div id="shop" class="hidden lg:block">
               <span class="block p-2 hover:underline">Gift cards</span>
               <span class="block p-2 hover:underline">Discounts</span>
               <span class="block p-2 hover:underline">Deals</span>

           </div>
           </div>

          <div class="w-full text-white">
          <div class="w-full h-8 p-1 text-white block hover:bg-red-400" onclick="show('helpus');">
            <div class="float-left font-bold block">
               Help / Talk to us
            </div>
            <div class="float-right lg:hidden">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
            </div>
          </div>
             <!-- dropdown for know us -->
           <div id="helpus" class="hidden lg:block">
               <span class="block p-2 hover:underline">Help center</span>
               <span class="block p-2 hover:underline">FAQs</span>
               <span class="block p-2 hover:underline" onclick="showContents('contactModal');">Contact Us</span>
               <span class="block p-2 hover:underline">Track My Order</span>
               <span class="block p-2 hover:underline">Shipping &amp; Delivery</span>
               <span class="block p-2 hover:underline">Returns Center</span>


            </div>
           </div>



           <div class="w-full text-white p-4">
              <div class="text-center">
                  <button class="rounded-full p-2 border-4 font-bold border-white"> App Launching Soon </button>
              </div>
              <div class="text-center mt-6">
               <a href="https://www.instagram.com/pilollo_tribe"><i class="ion-logo-instagram text-4xl font-bold mr-6"></i></a>
               <a href="https://www.instagram.com/pilollo_tribe"><i class="ion-logo-facebook text-4xl font-bold mr-6"></i></a>
               <a href="https://www.instagram.com/pilollo_tribe"><i class="ion-logo-twitter text-4xl font-bold mr-6"></i></a>
               <a href="https://www.instagram.com/pilollo_tribe"><i class="ion-logo-youtube text-4xl font-bold"></i></a>
              </div>
              <div class="text-center">
                  <h2 class="block">Contact Us</h2>
                  <a href="tel:050 155 7462"><span class="font-bold pt-2 block"><i class="icon-phone text-xl"></i>
          050 155 7462</span></a>
          <a href="tel:0247833618"><span class="font-bold pt-2 block"><i class="icon-phone text-xl"></i>
          (+233)-24-783-3618</span></a>
          <a href="https://wa.me/message/H5N4G7S4UIB2N1"><span class="font-bold pt-2 block"><i class="icon-whatsapp text-xl"></i> 050 155 7462</span></a>
              </div>
           </div>
        </div>
     </section>
   
    </div>
</template>
    <script setup>
</script>
<style scoped>
.footerBg {
  background-image: url("~/assets/footer-bg.png");
}
</style>