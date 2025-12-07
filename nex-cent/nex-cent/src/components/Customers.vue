<script setup>
import CustomersImage from '../assets/CustomersImage.jpg'
import logo1 from '../assets/ClientLogo1.webp'
import logo2 from '../assets/ClientLogo2.webp'      
import logo3 from '../assets/ClientLogo3.webp'
import logo4 from '../assets/ClientLogo4.webp'
import logo5 from '../assets/ClientLogo5.webp'
import logo6 from '../assets/ClientLogo6.webp'
import logo7 from '../assets/ClientLogo7.webp'
import Ptag from './Ptag.vue'

const clientLogos = [logo1, logo2, logo3, logo4, logo5, logo6, logo7];
const pTagText = 'Maecenas dignissim justo eget nulla rutrum molestie. Maecenas lobortis sem dui, vel rutrum risus tincidunt ullamcorper. Proin eu enim metus. Vivamus sed libero ornare, tristique quam in, gravida enim. Nullam ut molestie arcu, at hendrerit elit. Morbi laoreet elit at ligula molestie, nec molestie mi blandit. Suspendisse cursus tellus sed augue ultrices, quis tristique nulla sodales. Suspendisse eget lorem eu turpis vestibulum pretium. Suspendisse potenti. Quisque malesuada enim sapien, vitae placerat ante feugiat eget.  Quisque vulputate odio neque, eget efficitur libero condimentum id. Curabitur id nibh id sem dignissim finibus ac sit amet magna.'
const layoutSize='!w-[15.608rem] md:!w-[24.208rem] lg:!w-[32.541rem]'
</script>

<template>

    <section class="w-full bg-[#F5F7FA] py-10 px-4 md:px-10 lg:px-20">
        <div class=" flex items-center justify-center gap-10">
            <img class="
            w-[6.876rem]
            md:w-[10.134rem]
            lg:w-[14.182rem]
            h-[6.876rem]
            md:h-[10.134rem]
            lg:h-[14.182rem]
            rounded-[0.348rem]
            shadow-[0_0.348rem_0.696rem_0_#ABBED166]
            opacity-100
            " :src="CustomersImage" alt="image">
            <div class=" flex flex-col gap-1 md:gap-3 lg:gap-5">
                <Ptag class="font-medium tracking-normal align-middle p-layout-size" :text="pTagText"/>
                <Ptag class="tracking-normal align-middle font-semibold p-layout-size !text-[#4CAF4F]  " :text="'Tim Simth'"/>
                <Ptag class="trackin-normal align-middle p-layout-size text-[#89939E]" :text="'British Dragon Boat Racing Association'"/>
                <div class="flex items-center">
                    <div class="grid grid-cols-7 gap-4 ">
                        <img v-for="value in clientLogos" :src="value" class="h-[0.535rem] md:h-[1.2rem] lg:h-12 object-contain" alt="">
                    </div>
                    <Ptag class="font-semibold ml-1 !text-[#4CAF4F] !w-[3.922rem] md:!w-[6.034rem] lg:!w-[8.179rem]" :text="'Meet All Customers →'"/>
                </div>
            </div>
        </div>
    </section>

</template>