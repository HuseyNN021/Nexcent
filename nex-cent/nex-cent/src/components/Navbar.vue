<script setup>
import logo from '../assets/Logo.webp'
import Button from './Button.vue'

</script>

<template>

    <header 
  class="w-full h-auto flex justify-between items-center 
        px-6 md:px-[6.264rem] py-[0.696rem] gap-[2.740rem] "
>

  <!-- LOGO -->
  <div class="shrink-0">
    <img 
      :src="logo" 
      alt="logo" 
      class="w-12 md:w-20 lg:w-[6.6rem] h-auto"
    >
  </div>

  <!-- NAVIGATION -->
  <nav class="flex items-center gap-6">

    <ul class="hidden md:flex justify-between items-center 
               gap-6 text-sm font-medium leading-5 text-gray-700">
      <li>Home</li>
      <li>Features</li>
      <li>Community</li>
      <li>Blog</li>
      <li>Pricing</li>
    </ul>

    <Button class="w-16! md:w-22! lg:w-40!" :text="'Register Now →'" />
  </nav>
  
</header>


</template>