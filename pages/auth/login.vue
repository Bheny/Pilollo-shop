<template>
  <div class="pt-40 h-full lg:h-screen bg-white opacity-100 z-30  pb-24 w-full">
    <div class="text-center p-10">
      <h2 class="text-2xl font-bold text-slate-700">LOGIN</h2>
    </div>
    <div class="md:flex">
      <div class="hidden md:block w-2/3 h-screen border-b bg-cover p-12 flex">
        <img src="~/assets/login.png" class="w-64 h-64" />
      </div>
      <div class="pt-0">
        <div class="hidden lg:block pt-2">
          <img src="~/assets/Pilollo.png" class="w-40" />
        </div>
        <div class="hidden">
          <span
            ><a href="/social-auth/login/facebook/"
              >click to login with facebook
            </a></span
          >
        </div>
        <div>
          <div class="p-4 text-lg">
            <span
              >welcome <b id="wname">Back</b> 🤗, care for ride through our
              village .</span
            >
          </div>
          <!---->
          <!---->
          <div class="w-full p-4">
            <input
              type="text"
              placeholder="Username or Email"
              required="required"
              class="p-2 text-black border-b-2 w-full focus:border focus:border-black"
            />
          </div>
          <div class="w-full p-4">
            <input
              type="password"
              placeholder="Password"
              required="required"
              class="p-2 text-black border-b-2 w-full focus:border focus:border-black"
            />
          </div>
          <div class="w-full p-4">
            <div class="inline-block">
              <input type="checkbox" />
              <span class="ml-3 text-sm">Remember me </span>
            </div>
            <div class="float-right">
              <a href="/password_reset/"
                ><span class="text-sm text-gray-600 underline"
                  >Forgot Password ?</span
                ></a
              >
            </div>
          </div>
          <div class="p-4">
            <button
              class="rounded-lg p-2 w-full bg-red-700 text-white font-bold hover:bg-white hover:text-red-700 hover:border-red-700 border"
            >
              submitting...
            </button>
          </div>
          <nuxtLink to="/auth/register">

          <p
            class="focus:text-red-700 text-center mt-4"
          >
            Is this your first time 😃 ? <span class="text-blue-400 underline">Click to Join Us</span>
          </p>
          </nuxtLink>
        </div>
      </div>
    </div>

  </div>
</template>

<script setup>
definePageMeta({
  layout: 'auth'
})
</script>
