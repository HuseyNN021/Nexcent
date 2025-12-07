<script setup>
import { defineProps } from 'vue';
const props = defineProps({
    text: {
        type: String,
        required: true
    }
});
</script>

<template>

            <button class="
            w-[3.125rem]
            md:w-[4.167rem]
            lg:w-[6.597rem]
            h-[1.1rem]
            md:h-[1.667rem]
            lg:h-[2.281rem]
          gap-[0.435rem]
          px-[0.609rem]
            md:px-3.5
          lg:px-[1.392rem]
            py-[0.348rem]  
            md:py-[0.522rem]
          lg:py-[0.609rem]
          rounded-[0.173rem]
          bg-[#4CAF4F]
          opacity-100
          font-inter
          font-medium
          text-[0.334rem]
          md:text-[0.5rem]
          lg:text-[0.696rem]
          leading-[0.47rem]
          lg:leading-[1.044rem]
          tracking-normal
          text-center
          align-middle
          text-white      
          "
          
          >{{ props.text }}</button>
</template>