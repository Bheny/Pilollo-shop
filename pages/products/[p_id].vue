<template>
    <div class="pt-16">
      <div class="pt-4 lg:flex lg:p-2">
      <section class="lg:w-1/2 lg:h-screen pt-4">
        <div class="scroll w-full mb-4 relative ">
        <img id="0" :src="product.image" class="w-full">
        
        
        
        
        <div class="mt-4 absolute text-center w-full top-0 my-1 mx-1">
               <div class=" mr-2 pt-1 bg-white w-8 h-8 rounded-full float-right" onclick="like(99);">

                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" :class="[]" class="mx-auto  w-6 h-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z" />
</svg>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="hidden w-5 h-5">
  <path d="M9.653 16.915l-.005-.003-.019-.01a20.759 20.759 0 01-1.162-.682 22.045 22.045 0 01-2.582-1.9C4.045 12.733 2 10.352 2 7.5a4.5 4.5 0 018-2.828A4.5 4.5 0 0118 7.5c0 2.852-2.044 5.233-3.885 6.82a22.049 22.049 0 01-3.744 2.582l-.019.01-.005.003h-.002a.739.739 0 01-.69.001l-.002-.001z" />
</svg>

             </div>
             </div>
      </div>
      <div class="w-full p-2 flex overflow-x-scroll ">
        <span class="border-b border-black mr-2 rounded-lg inline-block">
          
          <img :src="product.image" class="h-16 w-16 rounded-lg bg-cover" onclick="view(0);">
          
        </span>
        
        
        
        
        
      </div>
      </section>
      <section class="w-full lg:w-2/3 lg:ml-32">
        <div class="p-2">
        <div class="w-full">
           <div class="w-1/2 inline-block">
            <span class="text-xl block">{{product.title}}</span>

           </div>
           <div class="float-right">
             <span class="block text-xl text-red-700 ">
                
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 inline h-5">
              <path fill-rule="evenodd" d="M10.868 2.884c-.321-.772-1.415-.772-1.736 0l-1.83 4.401-4.753.381c-.833.067-1.171 1.107-.536 1.651l3.62 3.102-1.106 4.637c-.194.813.691 1.456 1.405 1.02L10 15.591l4.069 2.485c.713.436 1.598-.207 1.404-1.02l-1.106-4.637 3.62-3.102c.635-.544.297-1.584-.536-1.65l-4.752-.382-1.831-4.401z" clip-rule="evenodd" />
            </svg> 


                <i class="">{{product.rating.rate }}  ({{product.rating.count}})</i>
              </span>
           </div>
        </div>
        <div class=" mb-2">
          <span class="text-sm inline-block">5 sales</span>

        </div>
        <div class="mb-2 rounded-full bg-yellow-400 w-1/2 flex">
          <img src="/static/img/store.png" class="w-4 h-4 mt-1 ml-2 mr-2">
            <span class="block">Pilollo tribe</span>
        </div>
        <div class="w-full mb-16">
          <div class="float-left text-xl font-extrabold">
            <span class="font-extrabold text-xl block inline-block">GHC 105.00</span>
                 

          </div>
            <div class="float-right">
              
              <span class="text-green-600">In stock</span>
              
            </div>
        </div>
        <div class="w-full">
          <form action="/cart/add/99/" method="POST">
            <input type="hidden" name="csrfmiddlewaretoken" value="ZCBcgL6bTgdkiPWdoxkiS8PGn1d6YLWxAADLuZwYLX09vgsyC0X6jqleIgTFaGDy">
            <div class="mb-2 w-full">
              <label class="text-sm focus:text-gray-800 block">SIZE</label>
              <select name="size" class="w-full p-2 rounded-lg">
                <option value="Small">Select an option</option>
                
                  
                     <option value="S">S</option>
                  
                     <option value="M">M</option>
                  
                     <option value="L">L</option>
                  
                     <option value="XL">XL</option>
                  
                     <option value="XXL">XXL</option>
                  
                

                </select>
                </div>
                <div class="mb-4">
                  <label class="text-sm focus:text-gray-800">COLOR</label>
                  <select name="color" class="w-full p-2 rounded-lg">
                    <option value="black">Select an option</option>
                   
                  </select>
                </div>
                
                <div onclick="showContents('customBox');" class="mb-2  flex">
                      <span class="text-sm p-2 bg-gray-400 hover:bg-gray-600 rounded-lg flex">Add your personalization(optional)<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg></span>

                </div>

                <div id="customBox" class="hidden mb-2">
                  <label class="text-sm text-gray-700 block">Enter your customed message here:</label>
                  <label class="text-sm text-gray-700 block">"Just tell us what you want and how you want it "</label>

                  <textarea name="message" class="w-full p-2 border rounded-lg"></textarea>

                </div>
                
                <div class="mb-2">
                  <label class="text-sm focus:text-gray-800">QUANTITY</label>
                  <select name="quantity" class="w-full p-2 rounded-lg">
                     <option value="1">1</option>
                     <option value="2">2</option>
                     <option value="3">3</option>
                     <option value="4">4</option>
                     <option value="5">5</option>
                     <option value="6">6</option>
                     <option value="7">7</option>
                     <option value="8">8</option>
                     <option value="9">9</option>

                  </select>
                </div>
                <div class="text-center">
                  <button type="submit" class="bg-gray-200 p-2 text-black font-extrabold rounded-full w-full hover:bg-white hover:text-red-700 border border-red-700 focus:outline-none "> <svg class="w-6 h-6 inline-block" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path strokelinecap="round" strokelinejoin="round" strokewidth="{2}" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>Add To Cart </button><br>
                  <input id="buy_now" type="text" name="direct" value="False" class="hidden">

                   <button onclick="document.getElementById('buy_now').value = 'True';" type="submit" class="bg-red-700 p-2 mt-2 text-white font-extrabold rounded-full w-full hover:bg-white hover:text-red-700 border border-red-700 focus:outline-none "> <svg class="w-6 h-6 inline-block" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path strokelinecap="round" strokelinejoin="round" strokewidth="{2}" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>Buy Now </button>


                </div>
              </form>
              </div>
              <div class="pt-4" style="background-image: url(/static/img/3.PNG);">
                <div class="w-full h-12  text-black block p-2 hover:bg-gray-100" onclick="show('itemdetails'),rotate('itemdetails-svg');">
                <div class="float-left font-extrabold">
                    Item Details
                </div>
                <div class="float-right">
                  <svg id="itemdetails-svg" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                </div>
               </div>
               <!-- dropdown for know us -->
           <div id="itemdetails" class="hidden">
              <span>Handmade</span>
              <div class="mb-4">
                <span class="text-gray-800 block">Description</span>
                <span class="block pb-2">
                  Bomber jacket
                </span>
                <span class="mt-2">
                    Materials Used include: Ankara fabric
                </span>
              </div>
           </div>

               <div class="w-full h-12  text-black block p-2 hover:bg-gray-100" onclick="show('shipping');">
                <div class="float-left font-extrabold">
                    Shipping and Return Policies
                </div>
                <div class="float-right">
                  <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                </div>
               </div>

                <!-- dropdown for shopping -->
           <div id="shipping" class="hidden">

              <div class="mb-4">
                <span class="text-gray-800 block">Ready to ship in </span>
                <span class="text-lg block mb-4">
                 4 - 7 business days
                </span>
                <span class="text-gray-800 block">Cost for one to Ship</span>
                <span class="text-lg">
                  GHC 
                </span>
                 <span class="text-gray-800 block">Cost for additional to Ship</span>
                <span class="text-lg">
                  GHC 
                </span>
              </div>
           </div>

               <div class="w-full h-12  text-black block p-2 hover:bg-gray-100" onclick="show('contact');">
                <div class="float-left font-extrabold">
                    Contact the Seller
                </div>
                <div class="float-right">
                  <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                </div>
               </div>

                <!-- dropdown for know us -->
           <div id="contact" class="hidden">

              <div class="mb-4 flex">
                <div>
                  <img src="/media/default.png" class="w-16 h-16">
                </div>
                <div class="ml-4 mb-2">
                  <span class="text-2xl block">Komla1</span>
                  <span>Owner of Pilollo tribe</span>
                </div>
              </div>
              <div class="mb-4 flex">
                <div class="float-left mr-32 text-center ">
                  <span class="block">Sales</span>
                  <span>5</span>
                </div>
                <div class="float-right text-center">
                  <span class="block">On pilollo since</span>
                  <span>June 10, 2021, 1:45 p.m. </span>
                </div>
              </div>
              <div>
                <span class="block text-sm text-gray-800">Located at</span>
                <span class="text-lg">Accra</span>
              </div>
              <div class="p-2 text-center">
                  <button class="p-2 text-black font-extrabold rounded-full w-full bg-white text-red-700 border border-red-700 foucus:rounded-full focus:outline-none "> Message Komla1 </button>
              </div>
           </div>
            <div class="mt-6">
              <div class="inline-block pl-4">
                 <span class="text-red-700 block">
                  
                <i class="ion-ios-star-half "></i> 
                <i class="ion-ios-star-outline "></i> 
                <i class="ion-ios-star-outline "></i> 
                <i class="ion-ios-star-outline "></i> 
                <i class="ion-ios-star-outline "></i>


               </span>
                <i class="">0 Reviews </i>

              </div>

                <div class="float-right">

                   

                </div>
               </div>

               <div class="w-full mt-4 flex p-2 border-b">
                 <div class="border-b-2 hover:border-black w-1/2 p-2" onclick="showItemReview();">
                  Item reviews <span class="rounded-full p-1 bg-gray-200">0</span>
                 </div>
                 <div class="border-b-2  p-2 w-1/2 hover:border-black" onclick="showShopReview();">
                  Shop reviews <span class="rounded-full p-2 bg-gray-200"> </span>
                 </div>
               </div>

               <!-- products reviews displayed by default but hidden when shop reviews is tapped -->
               <div id="itemreviews" class="w-full h-64 p-2 overflow-y-scroll">
                
                <div class="w-full flex border mb-4 rounded-lg p-2">
                <div class="w-2/4 lg:w-1/6">
                  
                  <img src="~/assets/ella.jpg" class="rounded-full w-12 h-12">
                  
                </div>
                <div class="ml-2">
                <span class="text-sm text-gray-700 block">
                  webmaster posted: 1&nbsp;year, 4&nbsp;months
                </span>
                <div class=" flex">

                <span class="text-red-700 block">
                  
				<i class="ion-ios-star  "></i> 
                <i class="ion-ios-star  "></i> 
                <i class="ion-ios-star  "></i> 
                <i class="ion-ios-star  "></i> 
                <i class="ion-ios-star-outline  "></i>

               </span>
               </div>
               <div>
                <p class="mb-4 flex-wrap">
                  Awesome bag , still rocking it and my friends still give me the "nod" every time i pass by . Kudos guys
                </p>
               </div>
               <div>
                 <span class="text-sm text-gray-800"><span id="2">0</span>  found this review helpful </span>
               </div>
               <div>
                  
                    <a href="/Products/helpful/2/"></a>
                  <button id="helpful" type="button" onclick="Increase(2);" class="rounded p-2 text-sm mr-2 border border-blue-700">

                    Helpful
                  </button>
                  
                  <button class="border-l rounded p-1 text-sm">  <svg viewBox="0 0 20 20" fill="currentColor" class="chat-alt2 inline-block w-6 h-6"><path d="M2 5a2 2 0 012-2h7a2 2 0 012 2v4a2 2 0 01-2 2H9l-3 3v-3H4a2 2 0 01-2-2V5z"></path><path d="M15 7v2a4 4 0 01-4 4H9.828l-1.766 1.767c.28.149.599.233.938.233h2l3 3v-3h2a2 2 0 002-2V9a2 2 0 00-2-2h-1z"></path></svg>Comment</button>
                  <button class="border-l  rounded p-1 text-sm">Report</button>
               </div>
                <div id="comment" class="hidden p-2 flex rounded-lg">
                  <div class="inline-block pt-2 w-6">
                    <img src="" class="rounded-full w-6 h-6">
                  </div>
                  <div>
                    <input type="text" name="comment" placeholder="write a comment on this review" class="p-2 border-b">
                  </div>
               </div>
               </div>
              </div>
                
               </div>

               <div id="shopreviews" class="hidden">

                
               </div>
              </div>
            </div>
            
      </section>
     
    </div>
    <section class="p-2 bg-yellow-200">
			<div class="p-2 flex w-fulll">
				<div class="w-3/5 mr-12">
					<h2 class="text-xl">Other Cardigans you may like. </h2>
				</div>
				<div class="text-right pt-8 ">
					<span class="text-base font-bold">see more</span>
				</div>
			</div>
			<div class="p-2">
				<div class="scroll">
					
				</div>
			</div>
		</section>
    <section class="p-2 bg-yellow-200">
      <div class="p-2 flex w-fulll">
        <div class="w-3/5 mr-12">
          <h2 class="text-xl"> Buyers who bought this also bought. </h2>
        </div>
        <div class="text-right ">
          <span class="text-base font-bold">see more</span>
        </div>
      </div>
      <div class="p-2">
        <div class="scroll">
          
             <div class="item">
                
                  
            <img :src="product?.image" class="rounded-lg w-32 h-32 object-cover object-center mr-2" width="200" height="200">
            
          
             </div>
          
        </div>
      </div>
    </section>
    </div>

  </template>
  
  <script setup>
    const { p_id } = useRoute().params

    const { data: product} = await useFetch(`https://fakestoreapi.com/products/${p_id}`)

    console.log(p_id)
  </script>