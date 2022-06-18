<template>
  <div
    class="lg:w-1/3 w-full mx-auto drop-shadow-lg bg-white rounded-lg p-3 mb-4"
  >
    <div class="grid grid-cols-3">
      <div
        class="pr-2 bg-[url('@/assets/song.jpg')] h-24 w-24 bg-cover rounded-lg"
      >
        <img src="@/assets/play.svg" class="mx-auto mt-7" />
      </div>
      <div class="col-span-2">
        <div class="font-medium text-xs">Travie Mc Coy</div>
        <div class="font-bold text-sm h-14">name of the song</div>
        <div class="flex flex-row justify between">
          <div class="flex-1">
            <span class="bg-green-500 px-3 py-1 text-xs text-white rounded-full"
              >Pop</span
            >
          </div>
          <div class="flex-1 text-right">
            <img class="pr-2 inline" src="@/assets/dollar.svg" />
            <span class="text-[#f5b014] text-xs text-semi-bold pt-2">1.9</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
