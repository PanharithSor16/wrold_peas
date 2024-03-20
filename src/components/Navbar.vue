<script setup lang="ts">
import { ref } from 'vue';

const navs = ref(['Shop', 'NewStand', 'Who we are', 'my profile'])
const togglebtn= ref(true);
const order = ref([])
</script>
<template>
    <section class="flex flex-row m-5 w-6/8 place-content-between ">
        <div class=" text-green-400 font-medium text-4xl">WorldPeas</div>
        <div class="flex flex-row ">
            <ul class="list-none flex flex-row ml-4 items-center invisible sm:visible">
                <li class="ml-4" v-for="(nav, index) in navs" :key="index">{{ nav }}</li>
            </ul>
            
            <button class="sm:ml-4 bg-green-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
                Basket {{ order.length }}
            </button>
        </div>
    </section>
</template>