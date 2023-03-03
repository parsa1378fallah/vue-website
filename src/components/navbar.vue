<template>
  <header>
    <nav class="flex items-center w-full h-16 bg-blue-900">
      <div class="logo mx-3 flex flex-col gap-1.5 cursor-pointer">
        <div v-for="item in 3" :key="item" class="w-6 h-0.5 bg-white"></div>
      </div>
        <ul class="flex gap-4 lg:gap-8   text-lg text-white mx-10 hidden sm:flex">
            <li v-for="item in data.navbar" :key="item.id">{{item.key}}</li>
        </ul>
        <div class="text-box w-4/12 hidden lg:flex">
          <input type="text" placeholder="جستجو..." class="py-2 px-2 rounded-md w-full bg-gray-100 text-black outline-none">
        </div>
        <ul class="hidden sm:flex gap-2 text-lg text-black mr-auto ml-4 ">
          <li v-for="item in data.register" :key="item.id">
            <button class="py-1 px-3 rounded-lg bg-blue-100">
              {{item.key}}
            </button>
          </li>
        </ul>
    </nav>
  </header>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router';
import data from '../data/fa.json'
console.log(data.navbar)
</script>

<style>

</style>