<script setup lang="ts">
import { ref } from "vue";
import CardItem from "./CardItem.vue";

var currentDate = new Date();
console.log(currentDate);
const isActive = true;
const btnfiter = ref(["Default", "A-Z", "list-view"]);
// function active() {
    
// }
</script>
<template>
  <section class="m-5 w-6/8 place-items-center">
    <div class="mt-10 flex flex-row place-content-between">
      <div class="flex flex-row items-center">
        <h2 class="text-3xl font-normal">Product</h2>
        <h3 class="ml-10 self-end invisible sm:visible" >{{ currentDate }}</h3>
      </div>
      <div>
        <button
          class="ml-4 bg-green-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded invisible sm:visible"
          :class="isActive"
          v-for="(btn, index) in btnfiter"
          :key="index"
        >
          {{ btn }}
        </button>
      </div>
    </div>
    <hr class="my-4 border-gray-300">
    <div class=" flex flex-col md:flex-row   sm:ml-[20%] ml-[10%] w-auto	">
      <CardItem/>
    </div>
  </section>
</template>
