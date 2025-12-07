<script setup>
import Button from './Button.vue'
import { defineProps } from 'vue';
import Ptag from './Ptag.vue';
const props = defineProps({
    img: {
        type: String,
        required: true
    },
    title: {
        type: String,
        required: true
    },
    description: {
        type: String,
        required: true
    }
});
</script>

<template>
    <section class="w-full mt-3  overflow-x-hidden">
  <div class="w-full flex justify-center items-center gap-6 lg:gap-12">

    <!-- IMAGE -->
    <div>
      <img :src="props.img" alt=""
        class="
          w-[9.542rem] h-[9.542rem]
          md:w-56 md:h-56
          lg:w-[19.208rem] lg:h-[14.312rem]
        ">
    </div>

    <!-- TEXT -->
    <div class="flex flex-col gap-4 md:gap-5 w-[13rem] md:w-[20rem] lg:w-[28.756rem]">

      <h2 class="
        font-inter font-semibold
        text-[0.751rem] md:text-[1.134rem] lg:text-[1.566rem]
        leading-[0.914rem] md:leading-[1.366rem] lg:leading-[1.914rem]
        text-[#4D4D4D]
      ">
        {{props.title}}
      </h2>

      <p class="
        font-inter 
        font-normal
        text-[0.291rem]
         md:text-[0.456rem] 
         lg:text-[0.609rem]
        leading-[0.418rem]
         md:leading-[0.656rem] 
         lg:leading-[0.87rem]
        text-[#717171]
      ">
        {{ props.description }}
      </p>
      <Button :text="'Learn More'"/>
    </div>

  </div>
</section>
</template>