<script setup>
import achievementImg1 from '../assets/AchievementImg1.png'
import achievementImg2 from '../assets/AchievementImg2.png'
import achievementImg3 from '../assets/AchievementImg3.png'
import achievementImg4 from '../assets/AchievementImg4.png'
import Htag2 from './Htag2.vue'
import Ptag from './Ptag.vue'
const achievementData=[
    {
        img: achievementImg1,
        value: '2245341',
        title: 'Members'
    },
    {
        img: achievementImg2,
        value: '46,328',
        title: 'Clubs'
    },
    {
        img: achievementImg3,
        value: '1,234',
        title: 'Event Bookings'
    },
    {
        img: achievementImg4,
        value: '128913',
        title: 'Payments'
    },
]
</script>

<template>

   <section class="w-full mt-5 bg-[#F5F7FA] py-10 px-6 lg:px-20">
      <div class="flex flex-col md:flex-row lg:flex-row justify-center items-center gap-10">

        <!-- LEFT TEXT -->
        <div>
          <Htag2 class="text-start">
            Helping a local <br>
            <span class="text-[#4CAF4F]">business reinvent itself</span>
          </Htag2>

        
          <Ptag class="text-[#18191F] mt-3 !w-[13rem] md:!w-[20rem] lg:!w-[23rem]" :text="'We reached here with our hard work an dedication'"/>
        </div>

        <!-- RIGHT GRID -->
        <div class="grid grid-cols-2 gap-x-10 gap-y-6">

          <div 
            v-for="value in achievementData" 
            :key="value.title"
            class="flex items-center gap-3">

            <img 
              :src="value.img" 
              :alt="value.title"
              class="w-[1.2rem] md:w-[1.6rem] lg:w-[2rem]">
            
            <div>
              <p class="
              font-inter 
              font-bold
              text-[0.584rem]
              md:text-[0.734rem]
              lg:text-[0.9rem] 
              md:text-[1.1rem] 
              lg:text-[1.2rem]
              leading-[0.734rem] 
              md:leading-[0.934rem]
              lg:leading-[1.2rem]
              md:w-[5.125rem]
              lg:w-[8.25rem]
              h-[0.8125rem]
              md:h-[1.125rem]
              lg:h-[1.625rem]
              text-[#4D4D4D]">
                {{ value.value }}
              </p>
              <span class="font-inter font-normal
                text-[0.456rem] md:text-[0.556rem] lg:text-[0.609rem]
                text-[#717171]">
                {{ value.title }}
              </span>
            </div>

          </div>

        </div>

  </div>
</section>

</template>