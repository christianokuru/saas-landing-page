<script setup>
import LogoComponent from "@/components/custom/LogoComponent.vue";

const navlinks = [
  { text: "About", route: { name: "about" } },
  { text: "Product", route: { name: "product" } },
  { text: "Resources", route: { name: "resources" } },
];
</script>

<template>
  <div class="w-[1680px]">
    <div class="flex items-center ml-[160px] my-[20px] border border-green-950">
      <!-- logo -->
      <div class="ml-[40px] my-[9.81px] w-[495.1px]">
        <logo-component />
      </div>
      <!-- navlinks -->
      <nav
        class="flex justify-between items-center h-[40px] py-[13px] px-[24px] mr-[215.5px]"
      >
        <router-link
          v-for="link in navlinks"
          :key="link.text"
          :to="link.route"
          class="text-[14px] font-medium text-[#F3F3F3] hover:text-[#C6F57A] space-x-[26px] mr-[42px]"
          active-class="text-[#C6F57A]"
        >
          {{ link.text }}
        </router-link>
      </nav>
      <!-- buttons -->
      <div class="">
        <button
          class="text-[#F3F3F3] text-[14px] border border-[#C6F57A] pl-[20px] pr-[36px] py-[9px] rounded-[38px]"
        >
          Get Started
        </button>
        <button
          class="bg-[#C6F57A] text-[14px] font-medium text-[#060807] px-[20px] py-[13px] rounded-[38px] ml-[8px]"
        >
          Contact Sales
        </button>
      </div>
    </div>
  </div>
</template>
