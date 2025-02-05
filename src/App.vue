<script setup>
import { RouterView } from 'vue-router'
import Navbar from "@/components/custom/Navbar.vue"
</script>

<template>
  <header>
    <Navbar />
  </header>
  <router-view />
</template>

