<template>
 <div>
  <TheNav />
  <router-view />
 </div>
</template>

<script setup>
 import { RouterView } from "vue-router"
 import TheNav from "./components/TheNav.vue"
</script>

<style>
 * {
  box-sizing: border-box;
 }
</style>
