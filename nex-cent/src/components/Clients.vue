<script setup>
import logo1 from '../assets/ClientLogo1.webp'
import logo2 from '../assets/ClientLogo2.webp'      
import logo3 from '../assets/ClientLogo3.webp'
import logo4 from '../assets/ClientLogo4.webp'
import logo5 from '../assets/ClientLogo5.webp'
import logo6 from '../assets/ClientLogo6.webp'
import logo7 from '../assets/ClientLogo7.webp'
import Htag2 from './Htag2.vue'
import Ptag from './Ptag.vue'

const clientLogos = [logo1, logo2, logo3, logo4, logo5, logo6, logo7];
const pTagText = ' We have been working with some Fortune 500+ clients'

</script>

<template>

  <section>
    <div class="flex flex-col items-center justify-center">
        <div class="flex flex-col justify-center items-center">
            <Htag2 class="w-[23.579rem] md:w-[34.264rem] lg:w-[48.289rem] h-3.75 md:h-5.5 lg:h-7.75" :text="'Our Clients'"/>
            <Ptag class="tracking-normal text-center" :text="pTagText"/>
        </div>
        <div>
            <div class="grid grid-cols-3 lg:grid-cols-7 gap-4 
            mt-8
            w-[23.579rem]
            md:w-[34.264rem]
            lg:w-[48.289rem]
            h-8
            md:h-16
            lg:h-20
            opacity-100
            mx-auto
            ">
                <div v-for="(logo, index) in clientLogos" :key="index" class="flex items-center justify-center -mt-3">
                    <img :src="logo" alt="Client Logo" class="h-[0.535rem] md:h-[1.2rem] lg:h-12 object-contain"/>
                </div>
            </div>
        </div>
    </div>
  </section>

</template>