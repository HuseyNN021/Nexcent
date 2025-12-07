<script setup>
import { defineProps } from "vue";

const props = defineProps({
  text: {
    type: String,
    default: ""
  }
});
</script>

<template>
  <h2
    class="font-inter font-semibold
           text-[0.751rem] md:text-[1.134rem] lg:text-[1.566rem]
           leading-[0.914rem] md:leading-[1.366rem] lg:leading-[1.914rem]
           tracking-normal text-center text-[#4D4D4D] opacity-100"
  >
    <!-- Əgər text props göndərilibsə onu göstər -->
    <span v-if="props.text">{{ props.text }}</span>

    <!-- Yox, əgər slot göndərilibsə slotu göstər -->
    <slot v-else></slot>
  </h2>
</template>
