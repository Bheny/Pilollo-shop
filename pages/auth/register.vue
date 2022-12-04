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
                      Join millions of designers sharing their expeiriences and
                      bonding with each other
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
                  <div class="mb-4">
                    <input
                      type="email"
                      placeholder="Email"
                      id="email"
                      required="required"
                      class="p-3 rounded-lg focus:border focus:bg-gray-300 border-b w-full"
                    />
                    <span class="text-xs text-gray-500 pl-2 inline-block"
                      >Confirmation link will be sent to it</span
                    >
                    <button
                      id="emailbtn"
                      type="button"
                      onclick="showContents('accnt');showContents('emailbtn');"
                      class="hidden p-2 bg-red-700 w-full rounded-lg text-white font-extrabold mt-4"
                    >
                      Continue
                    </button>
                  </div>
                  <div id="accnt">
                    <div class="w-full mb-4">
                      <input
                        type="text"
                        placeholder="Username"
                        id="id_uname"
                        required="required"
                        class="p-3 rounded-lg border-b w-full focus:border focus:bg-gray-300"
                      />
                      <span id="uname_msg" class="text-gray-700 text-sm"
                        >make it a unique one</span
                      >
                    </div>
                    <div class="mb-4">
                      <div class="bg-white border-b w-full focus:border">
                        <input
                          type="password"
                          placeholder="Password"
                          id="pwd1"
                          required="required"
                          class="p-3 rounded-lg inline-block w-5/6"
                        />
                        <span
                          id="pwd1m"
                          onclick="change('pwd1','pwd1m');"
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
                    </div>
                    <div class="mb-4">
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
                    </div>
                    <div class="mb-4">
                      <label class="w-full"
                        ><input
                          type="checkbox"
                          required="required"
                          class="border-b"
                        />
                        <span class="text-sm"
                          >I agree to the terms and conditions</span
                        ></label
                      >
                    </div>
                    <button
                      type="submit"
                      class="p-2 bg-red-700 w-full rounded-lg text-white font-extrabold"
                    >
                      Join the tribe 🥳
                    </button>
                    <p
                      onclick="showContents('signup');showContents('login');"
                      class="text-red-700 text-center mt-4"
                    >
                      Are you already part of us ? then Login
                    </p>
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
definePageMeta({
  layout: 'auth'
})
</script>

