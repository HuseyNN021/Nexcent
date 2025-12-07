<script setup>
import { onMounted } from 'vue'
import logo from '../assets/Logo.webp'
import instagramIcon from '../assets/instagremIcon.png'
import SocialIcons from '../assets/SocialIcons2.png'
import youtubeIcon from '../assets/youtubeIcon.png'
import twitterIcon from '../assets/twitterIcon.png'
import Button from './Button.vue'
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(()=>{
  gsap.from('.footerTitle',{
    scrollTrigger: {
      trigger: ".footerGsap",
      start: "top 85%",
      toggleActions: "play none none none"
      // play = scroll-a çatanda animasiya et
      // none = başqa heç nə etmə
    },
    duration: 0.9,
    scale: 0.8,
    opacity: 0,
    y: 20,
    stagger: 0.18,
    ease: "power3.out"
  })
})
</script>

<template>

<section class="w-full mt-10 bg-[#ccd4df]">
  <div class="flex flex-col justify-center items-center">

    <div class="footerGsap flex flex-col items-center p-5">
      <h2 class="footerTitle font-inter font-semibold
        text-[1.566rem] md:text-[2.034rem] lg:text-[2.784rem]
        leading-[1.591rem] md:leading-[2.066rem] lg:leading-[3.306rem]
        text-[#263238] text-center
        w-[18.588rem] md:w-[26.146rem] lg:w-[38.588rem]">
        Pellentesque suscipit fringilla libero eu.
      </h2>

      <Button class="mt-6" :text="'Learn More'"/>
    </div>
    <div
      class="w-full bg-[#263238]
            flex flex-col lg:flex-row
            justify-center
            items-center   <!-- düzəldildi -->
            gap-10 lg:gap-[5.438rem]
            pt-[2.784rem] pb-[2.784rem]
            px-4 md:px-10 lg:px-[7.178rem]
            mt-3">

        <!-- 1. LOGO + SOCIAL -->
        <div
          class="flex flex-col
                w-28 md:w-44 lg:w-60
                gap-[0.834rem] md:gap-[1.2rem] lg:gap-[1.74rem]">

            <div class="flex items-center gap-2">
              <img src="../assets/Icon (11).png" alt="" />
              <p class="text-white font-bold">Nexcent</p>
            </div>

            <p class="font-inter font-normal text-[0.609rem] leading-[0.87rem] text-[#F5F7FA] w-[15.226rem]">
              Copyright © 2020 Landify UI Kit.
            </p>

            <div class="flex gap-[0.696rem] mt-3">
              <img class="w-[1.392rem] h-[1.392rem]" src="../assets/youtubeIcon.png">
              <img class="w-[1.392rem] h-[1.392rem]" src="../assets/twitterIcon.png">
              <img class="w-[1.392rem] h-[1.392rem]" src="../assets/instagremIcon.png">
              <img class="w-[1.392rem] h-[1.392rem]" src="../assets/SocialIcons2.png">
            </div>
        </div>


        <!-- 2. COMPANY COLUMNS -->
        <div class="flex  gap-[5.438rem]">

          <div>
            <h2 class="font-inter font-semibold text-[0.87rem] leading-[1.218rem] text-white">Company</h2>
            <ul class="mt-2 space-y-2">
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">About us</li>
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">Blog</li>
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">Contact us</li>
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">Pricing</li>
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">Testimonials</li>
            </ul>
          </div>

          <div>
            <h2 class="font-inter font-semibold text-[0.87rem] leading-[1.218rem] text-white">Company</h2>
            <ul class="mt-2 space-y-2">
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">About us</li>
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">Blog</li>
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">Contact us</li>
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">Pricing</li>
              <li class="text-[#F5F7FA] text-[0.418rem] lg:text-[0.609rem]">Testimonials</li>
            </ul>
          </div>

        </div>


        <!-- 3. SUBSCRIBE SECTION -->
        <div class="flex flex-col gap-3
                    w-[11.09rem] md:w-52 lg:w-60">

          <h2 class="font-inter font-semibold text-[0.87rem] leading-[1.218rem] text-white">
            Stay up to date
          </h2>

          <div class="relative
                      w-[5.321rem] md:w-32 lg:w-full
                      h-[0.834rem] md:h-[1.2rem] lg:h-[1.740rem]
                      flex items-center">

            <input
              type="text"
              placeholder="Your email address"
              class="w-full h-full pl-3 pr-10
                    text-[0.291rem] md:text-[0.45rem] lg:text-[0.608rem]
                    bg-gray-600 rounded-[0.174rem] text-white placeholder:text-white/70"
            />

            <img
              src="@/assets/send.png"
              alt="send"
              class="absolute right-1 md:right-2 lg:right-3
                    cursor-pointer
                    w-[0.37rem] md:w-[0.57rem] lg:w-[0.783rem]"
            />
          </div>
        </div>

    </div>


  </div>
</section>


</template>