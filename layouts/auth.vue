<template>
    <div>
        <div class="w-full   p-4 fixed bg-white shadow-b-2xl">
          <div class="w-24 inline-block float-left relative">
            <NuxtLink to="/"><img src="~/assets/Pilollo.png" /></NuxtLink>
          </div>
          <div onclick="showContents('signup');" class="hidden float-right">
            <svg viewBox="0 0 20 20" fill="currentColor" class="x w-6 h-6">
              <path
                fill-rule="evenodd"
                d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                clip-rule="evenodd"
              ></path>
            </svg>
          </div>
        </div>
        <slot />
       
    </div>
</template>

<script setup>
</script>
