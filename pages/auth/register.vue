<template>
  <div>
    <div
      id="signup"
      class="h-full "
    >
      <div
        class=""
      >
        
        <section class="p-2 pt-12 overflow-y-scroll lg:pl-40 lg:pr-40">
          <div class="md:flex">
            <div class="pt-4">
              <div class="p-2">
                <div class="text-center w-full pt-4">
                  
                    <h6 class="text-gray-800 text-xl text-center mb-6">
                      Before We Begin ..
                    </h6>
                
                </div>
                <div id="noti" class="rounded-lg p-2 text-gray-800 text-center">
                  <!---->
                  <!---->
                </div>
                <div class="p-2 hidden">
                  <div class="w-full mb-4">
                    <button
                      class="bg-white p-2 rounded-full w-full border border-gray-700"
                    >
                      <i class="ion-logo-google text-2xl font-bold mr-2"></i>
                      <b class="text-lg">continue with Google</b>
                    </button>
                  </div>
                  <div class="w-full mb-4">
                    <button
                      class="bg-white p-2 rounded-full w-full border border-blue-700 text-blue-700"
                    >
                      <i class="ion-logo-facebook text-3xl font-bold mr-2"></i>
                      <b class="my-2 text-lg">continue with facebook</b>
                    </button>
                  </div>
                </div>
                <div class="hidden flex mt-2 w-full text-center">
                  <hr class="w-40 mr-2 mt-3" />
                  OR
                  <hr class="w-40 ml-2 mt-3" />
                </div>
                <form>
                  <input
                    type="hidden"
                    name="csrfmiddlewaretoken"
                    value="Ug6rKfZO6DUaVXMcuUpX5wg02X0K3rIIve80YtpBYkHZ8oixIn2LwOMyncGjfmpJ"
                  />
                  <div :class="[emailActive ? 'block':'hidden']" class="mb-4">
                    <input
                      type="email"
                      placeholder="Email"
                      v-model="email"
                      required="required"
                      class="p-3 rounded-lg focus:border focus:bg-gray-300 border-b w-full"
                    />
                    <div class="w-full px-auto">
                      <div class="mx-auto text-center">
                        OR
                      </div>
                    </div>
                    <input
                      type="text"
                      placeholder="Phone"
                      v-model="phone"
                      required="required"
                      class="p-3 rounded-lg focus:border focus:bg-gray-300 border-b w-full"
                    />
                    <span class="text-xs text-gray-500 pl-2 inline-block"
                      >Confirmation link will be sent to it</span
                    >
                    <button
                      type="button"
                      @click="next()"
                      class=" p-2 bg-red-700 w-full rounded-lg text-white font-extrabold mt-4"
                    >
                      Continue
                    </button>
                  </div>
                  <div id="accnt" class="w-full ">
                    <div :class="[emailActive || passwordActive ? 'hidden':'block']" class="w-full mb-4">
                      <input
                        type="text"
                        placeholder="Username"
                        id="id_uname"
                        v-model = "username"
                        required="required"
                        class="p-3 rounded-lg border-b w-full focus:border focus:bg-gray-300"
                      />
                      <span id="uname_msg" class="text-gray-700 text-sm"
                        >make it a unique one</span
                      >
                      <button
                      type="button"
                      @click="next()"
                      :class="[usernameTaken ? 'bg-red-700':'bg-green-500 text-white ']"
                      class=" p-2  w-full rounded-lg text-white font-extrabold mt-4"
                    >
                      {{btn}}
                    </button>
                    <button
                      type="button"
                      @click="back()"
                      class=" p-2 bg-gray-100 w-full rounded-lg text-gray-800 font-extrabold mt-4"
                    >
                      Back
                    </button>
                    </div>
                    <div :class="[passwordActive ? 'block':'hidden']" class=" mb-4">
                      <div class="bg-white border-b w-full focus:border">
                        <input
                          ref="passwordInput"
                          type="password"
                          placeholder="Password"
                          id="pwd1"
                          required="required"
                          v-model="password"
                          class="p-3 rounded-lg inline-block w-5/6"
                        />
                        <span
                          id="pwd1m"
                          @click="show"
                          class="text-xs underline pt-2 float-right pr-4"
                          >Show</span
                        >
                      </div>
                      <span class="pt-2 text-xs"
                        ><span class="text-xl text-gray-700 font-bold"
                          >Hint:</span
                        >
                        <ul>
                          <li>Not similar to personal information.</li>
                          <li id="length" class="text-gray-700">
                            must be more than 8 characters.
                          </li>
                          <li>Not a commonly used password.</li>
                          <li>Not entirely numeric.</li>
                        </ul></span
                      >
                      <div class="mt-6 mb-4">
                      <label class="w-full"
                        ><input
                          type="checkbox"
                          required="required"
                          class="border-b rounded-lg w-4 h-4 pt-2"
                          
                        />
                        <span class="text-sm"
                          >I agree to the terms and conditions</span
                        ></label
                      >
                    </div>
                    <div class="mt-6">
                      <button
                      :disabled="agreed"
                      type="submit"
                      class="p-2 bg-red-700 w-full rounded-lg text-white font-extrabold"
                    >
                      Join the tribe 🥳
                    </button>
                    <NuxtLink to="/auth/login">
                    <p
                      class="text-red-700 text-center mt-4"
                    >
                      Are you already part of us ? then Login
                    </p>
                  </NuxtLink>
                    </div>
                    </div>
                    <!-- <div class=" hidden mb-4">
                      <div class="bg-white border-b w-full focus:border">
                        <input
                          type="password"
                          placeholder="Confirm Password"
                          id="pwd2"
                          required="required"
                          class="p-3 rounded-lg border-b inline-block w-5/6"
                        />
                        <span
                          id="pwd2m"
                          onclick="change('pwd2','pwd2m');"
                          class="text-xs underline pt-2 float-right pr-4"
                          >Show</span
                        >
                      </div>
                      <span id="passwd_msg" class="text-gray-700 text-sm"
                        >Enter the same password as before, for
                        verification.</span
                      >
                    </div> -->
                    
                  </div>
                </form>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>
<script setup>
let emailActive = ref(true);
let usernameActive = ref(false);
let passwordActive = ref(false);
let email = ref('bernard.tay@htu.edu.gh')
let username = ref(null)
let usernameTaken = ref(true)
let btn = ref("continue")
const password = ref(null)
let phone =ref(null)
const passwordInput = ref(null)

// show password 
const show = () => { if(passwordInput.value.type=="text"){ passwordInput.value.type = "password"} else {passwordInput.value.type="text"}}
const next = () => {
  if(email.value || phone.value){
    emailActive.value = false

    // salutations.value = "Hey Benny! You're Back";
    // message.value = "Great to see you again, Enter your password to continue";
    // btn.value = "Enter Shop"
} 

if(username.value && btn.value != "Proceed"){
  //check from the backend if username exists
      usernameTaken.value = false
      btn.value = "Proceed"
} else if(btn.value == "Proceed"){
       passwordActive.value = true
} else {
  console.log("not valid")
}
}
const back = () => {
  if(emailActive.value == false){

    emailActive.value = true

    // salutations.value = "Hey Benny! You're Back";
    // message.value = "Great to see you again, Enter your password to continue";
    btn.value = "Continue"
} else {
  console.log("not valid")
}
}
definePageMeta({
  layout: 'auth'
})
</script>

