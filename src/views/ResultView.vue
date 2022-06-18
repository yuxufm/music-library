<script setup>
import Songs from "@/components/Songs.vue";
import { RouterLink } from "vue-router";
</script>

<script>
export default {
  data() {
    return {
      open: false,
    };
  },
};
</script>

<template>
  <nav>
    <div
      class="flex justify-between w-full bg-gradient-to-r from-[#712bda] to-[#a45deb] px-4 py-5"
    >
      <div>
        <img
          class="mx-auto cursor-pointer"
          alt="menu"
          src="@/assets/menu.svg"
        />
      </div>
      <div>
        <RouterLink to="/">
          <img class="mx-auto" alt="logo" src="@/assets/ngmusic.svg" />
        </RouterLink>
      </div>
      <div>
        <img
          class="mx-auto cursor-pointer"
          alt="search"
          src="@/assets/search.svg"
          @click="open = true"
        />
      </div>
    </div>
  </nav>
  <div class="flex flex-col justify-center px-4">
    <div class="mx-auto pt-10 mb-7">
      <span class="text-xs">Search result for:</span>
      <span class="text-[#7b34dd] font-bold pl-2">Jason Mraz</span>
    </div>
    <!-- list of songs -->
    <Songs />
    <Songs />
    <div class="text-center mt-5">
      <button
        class="transition-all hover:drop-shadow bg-[#e2e8f0] text-xs font-bold text-[#64748b] px-8 py-2 rounded-full"
      >
        Load More
      </button>
    </div>
  </div>

  <!-- search modal -->
  <div>
    <Teleport to="body">
      <div
        class="fixed inset-0 bg-[#1c1c2de6] overflow-y-auto h-full w-full"
        id="my-modal"
        v-if="open"
      >
        <img
          class="absolute top-10 right-10 cursor-pointer"
          src="@/assets/x.svg"
          @click="open = false"
        />
        <div class="absolute left-0 right-0 top-20 text-center mx-10">
          <h2 class="text-white font-bold text-lg mt-40">Search</h2>
          <div class="my-4">
            <input
              class="!outline-none w-full lg:w-1/3 rounded-full bg-white text-[#64748b] text-xs font-medium px-10 py-3 focus:border-white"
              placeholder="Artist / Album / Title"
            />
          </div>
          <div class="my-4">
            <RouterLink to="/result">
              <button
                class="transition-all hover:drop-shadow-lg lg:w-1/3 w-full rounded-full bg-gradient-to-r from-[#712bda] to-[#a45deb] text-sm font-medium px-10 py-3 text-white"
              >
                Search
              </button>
            </RouterLink>
          </div>
        </div>
      </div>
    </Teleport>
  </div>
</template>
