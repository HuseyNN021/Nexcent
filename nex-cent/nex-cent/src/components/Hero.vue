<script setup>
import heroImg from '../assets/Illustration.webp'
import Button from './Button.vue'
import Ptag from './Ptag.vue'
</script>

<template>

    <section  class="w-full
            gap-[4.524rem]
            pt-[4.176rem] pb-[4.176rem]
            px-4 md:px-[6.264rem]
            bg-[#F5F7FA]
            opacity-100">
        <div class="flex justify-center items-center">
            <div class="
                w-52
                md:w-[20rem]
                lg:w-[28.582rem]
                h-24
                md:h-36
                lg:h-[12.056rem]
                flex flex-col
                gap-[1.392rem]
                opacity-100
                ">
                <h1 class="font-inter
                    font-semibold
                    text-[1rem]
                    md:text-[1.5rem]
                    lg:text-[2.784rem]
                    leading-[1.334rem]
                    lg:leading-[3.306rem]
                    tracking-normal
                    w-52
                    md:w-[20rem]
                    lg:w-[28.582rem]
                    h-6
                    md:h-12
                    lg:h-26.5
                    opacity-100
                    ">
                    Lessons and insights <br> <span class="text-[#4CAF4F]">from 8 years</span>
                </h1>
                <Ptag class="trackin-normal !w-[13.709rem] md:!w-[20rem] lg:!w-[28.582rem]"  :text="'Where to grow your business as a photographer: site or social media?'"/>
                <Button :text="'Register'"/>
            </div>
            <img :src="heroImg" class="w-[10rem] md:w-52 lg:w-[17rem]" alt="Hero Image">
        </div>
    </section>


</template>