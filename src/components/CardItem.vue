<script setup lang="ts">
import { ref } from "vue";
import dragon from "../assets/khmer1.jpg";
import person from "../assets/khmer2.jpg";
import angkor from "../assets/khmer3.jpg";

const listCard = ref([
  { img: dragon, name: "dragon", price: "10$" },
  { img: person, name: "person", price: "10$" },
  { img: angkor, name: "Angkor", price: "10$" },
]);
</script>
<template>
  <div
    v-for="(item, index) in listCard"
    :key="index"
    class="max-w-[300px] pt-4 bg-white"
  >
    <img :src="item.img" class="m-2 max-w-[280px] rounded-md" />
    <h1 class="m-2 text-xl">{{ item.name }}</h1>
    <h3 class="m-2 text-green-400">{{ item.price }}</h3>
  </div>
</template>
