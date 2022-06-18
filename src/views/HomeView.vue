<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <div class="h-screen w-screen bg-gradient-to-b from-[#712bda] to-[#a45deb]">
    <div class="absolute left-0 right-0 top-1/3">
      <img class="mx-auto" alt="logo" src="@/assets/logo.svg" />
    </div>
    <div class="absolute left-0 right-0 bottom-20 text-center mx-10">
      <div class="my-4">
        <input
          class="!outline-none w-full lg:w-1/3 rounded-full bg-white text-[#64748b] text-xs font-medium px-10 py-3 focus:border-white"
          placeholder="Artist / Album / Title"
        />
      </div>
      <div class="my-4">
        <RouterLink to="/result">
          <button
            class="transition-all hover:drop-shadow-lg lg:w-1/3 w-full rounded-full bg-[#ffffff33] text-sm font-medium px-10 py-3 text-white"
          >
            Search
          </button>
        </RouterLink>
      </div>
    </div>
  </div>
</template>
