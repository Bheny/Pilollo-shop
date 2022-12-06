<template>
  <div class="pt-24 h-full lg:h-screen bg-white opacity-100 z-30  pb-24 w-full">
    <div class="hidden text-center ">
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
          <div class="p-4">
            <!-- <span
              >welcome <b id="wname">Back</b> 🤗, care for ride through our
              village .</span
            > -->
           
            <h2 class="text-lg font-bold">{{ salutations }}</h2>
            <span class="text-sm">{{ message }} </span>
          </div>
          <!---->
          <!---->
          <div :class="[ EmailActive ? 'hidden':'block' ]" class="w-full p-4">
            <input
              type="text"
              placeholder="Username or Email"
              required="required"
              class="p-2 text-black border-b-2 w-full focus:border focus:border-black"
              v-model="email"
            />
            <button
              class="mt-3 rounded-lg p-2 w-full bg-red-700 text-white font-bold hover:bg-white hover:text-red-700 hover:border-red-700 border"
              @click="checkEmail()">
             Continue
            </button>
          </div>
          <div  :class="[ EmailActive ? 'Block':'hidden' ]" class="w-full p-4">
            <input
              type="password"
              placeholder="Password"
              required="required"
              class="p-2 text-black border-b-2 w-full focus:border focus:border-black"
              v-model="password"
            />
            <div class="inline-block mt-2">
              <input type="checkbox" class="w-4 h-4 rounded-lg " />
              <span class="ml-3  text-sm">Remember me </span>
            </div>
            <div class="float-right">
              <a href="/password_reset/"
                ><span class="text-sm text-gray-600 underline"
                  >Forgot Password ?</span
                ></a
              >
            </div>
            <div class="w-full p-4">
            <button
              class="mt-3 rounded-lg p-2 w-full bg-red-700 text-white font-bold hover:bg-white hover:text-red-700 hover:border-red-700 border"
              @click="">
             {{ btn }}
            </button>
          </div>
          </div>
          
          <div class="p-4">
            
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
let EmailActive = ref(false)
let email = ref("bernard@tay.htu.gh")
let password = ref(null)
let btn = ref("Continue")

// const passwordActive = ref(false)
let salutations = ref("Sign In to continue ")
let message = ref("Sign In or Register with your email address")

const checkEmail = () => {
  console.log(typeof(email.value), email.value == 'bernard@tay.htu')
  if(email.value == 'bernard@tay.htu'){
    EmailActive.value = true
    salutations.value = "Hey Benny! You're Back";
    message.value = "Great to see you again, Enter your password to continue";
    btn.value = "Enter Shop"
}
}


definePageMeta({
  layout: 'auth'
})
</script>

<!-- <script >
export default({
  data(){
    return {
      usernameActive:true,
      passwordActive :false
    }
  },
  methods: {
    changeTo(item){
    console.log(item)
      if (item == 'password'){
          this.usernameActive = false;
          passwordActive = true;
      }
      if (item == "username"){
          usernameActive = true;
          passwordActive = false;
      }
  }
  }
})
</script> -->
