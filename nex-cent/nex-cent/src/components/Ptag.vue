<script setup>
import { defineProps } from 'vue';
const props=defineProps({
    text: {
        type: String,
        required: true
    }
})
</script>

<template>

    <p 
     class="font-inter 
            font-normal
            text-[0.334rem] 
            md:text-[0.556rem] 
            lg:text-[0.696rem]
            leading-[0.47rem]
            md:leading-[0.782rem] 
            lg:leading-[1.044rem]
            text-[#717171]
            w-full
            md:w-[34.264rem] 
            lg:w-[48.289rem]
            opacity-100
            mt-1">
        {{ props.text }}
    </p>
</template>