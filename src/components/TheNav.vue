<template>
 <div class="mx-auto">
  <nav class="p-5 bg-white flex justify-between items-center h-32">
   <router-link to="/home" class="cursor-pointer w-1/5">
    <span class="text-4xl font-serif font-bold">
     <img src="@/assets/logo.png" class="h-12 inline" />
     Parexellence
    </span>
   </router-link>
   <form method="GET" class="w-2/5">
    <div class="relative text-gray-600 focus-within:text-gray-400 w-full">
     <span class="absolute inset-y-0 left-0 flex items-center pl-2">
      <button type="submit" class="p-1 focus:outline-none focus:shadow-outline">
       <i class="fa-solid fa-magnifying-glass"></i>
      </button>
     </span>
     <input
      type="search"
      name="q"
      class="px-3 py-2 font-semibold border outline-none rounded-full w-full pl-10"
      placeholder="Search..."
      autocomplete="off"
     />
    </div>
   </form>
   <ul class="flex basis-1/4 justify-around w-2/5 items-center">
    <li>
     <router-link to="path" class="flex items-center">
      <div class="inline-block">
       <i class="fa-regular fa-circle-question text-3xl pr-4"></i>
      </div>
      <div class="inline-block">
       <span class="text-lg">Help is here</span>
       <p class="text-xs">0725-845-845</p>
      </div>
     </router-link>
    </li>
    <li>
     <router-link to="path">
      <i class="fa-regular fa-user text-2xl px-4"></i>
      Sign in
     </router-link>
    </li>
    <li>
     <router-link to="path">
      <i class="fa-solid fa-bag-shopping text-2xl px-4"></i> Cart
     </router-link>
    </li>
   </ul>
  </nav>
  <nav class="flex">
   <div
    class="group inline-block relative w-full"
    v-for="(item, index) in navTwo"
    :key="index"
   >
    <button class="py-2 px-4 rounded inline-flex items-center">
     <span class="mr-1 f">{{ item.title }}</span>
    </button>
    <ul class="absolute hidden text-gray-700 pt-1 group-hover:block w-full">
     <li class="">
      <a
       class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap"
       href="#"
       >{{ item.url }}</a
      >
     </li>
     <li class="">
      <a
       class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap"
       href="#"
       >Two</a
      >
     </li>
     <li class="">
      <a
       class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap"
       href="#"
       >Three is the magic number</a
      >
     </li>
    </ul>
   </div>
  </nav>
 </div>
</template>

<script setup>
 import { ref } from "vue"
 import { RouterLink } from "vue-router"
 const navTwo = ref([
  {
   title: "Featured",
   url: "/one",
  },
  {
   title: "Business Cards",
   url: "/two",
  },
  {
   title: "Marketing Materials",
   url: "/three",
  },
  {
   title: "Labels,Stickers,& Packaging",
   url: "/four",
  },
  {
   title: "Clothing & Bags",
   url: "/five",
  },
  {
   title: "Signs & Banners",
   url: "/five",
  },
  {
   title: "Invitations & Stationery",
   url: "/five",
  },
  {
   title: "Promotional Items",
   url: "/five",
  },
  {
   title: "Digital Marketing",
   url: "/five",
  },
  {
   title: "Design Services",
   url: "/five",
  },
 ])
</script>

<style></style>
