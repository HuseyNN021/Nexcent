<script setup>
import GroupImg from '../assets/GroupIcon.webp'
import MemberShipImg from '../assets/MembershipIcon.webp'
import AssociationImg from '../assets/AssociationIcon.webp'
import Ptag from './Ptag.vue'
import Htag2 from './Htag2.vue'
import { reactive } from 'vue'

const communitData=reactive([
    {
    img: MemberShipImg,
    title: 'Membership Organisations',
    description: 'Our membership management software provides full automation of membership renewals and payments'
    },
    {
    img: AssociationImg,
    title: 'National Associations',
    description: 'Our membership management software provides full automation of membership renewals and payments'
    },
    {
    img: MemberShipImg,
    title: 'Clubs And Groups',
    description: 'Our membership management software provides full automation of membership renewals and payments'
    },
])
const pTagText = 'Who is Nextcent suitable for?';   
</script>

<template>

   <section class="w-full bg-[#F5F7FA] p-4">
      <div class="flex flex-col justify-center items-center gap-3">
            <div class="flex flex-col justify-center items-center text-center gap-3">
                <Htag2 class="w-[11.310rem] md:w-[34.264rem] lg:w-[48.289rem]" :text="' Manage your entire community in a single system'"/>
                <Ptag :text="pTagText" />
            </div>
            <div>
                <div class="grid grid-cols-3 justify-items-center items-center gap-8">
                    <div class="
                    w-[6.239rem]
                    md:w-[10rem]
                    lg:w-[13.008rem]
                    h-[5.45rem]
                    md:h-[8rem]
                    lg:h-[11.381rem]
                    gap-[0.167rem]
                    md:gap-[0.24rem]
                    lg:gap-[0.348rem]
                    pt-[1.044rem]
                    pr-[1.392rem]
                    pb-[1.044rem]
                    pl-[1.392rem]
                    rounded-[0.348rem]
                    opacity-100
                    flex flex-col items-center justify-center
                    " 
                    v-for="value in communitData">
                        <img class="
                            w-[1.356rem]
                            md:w-[1.9rem]
                            lg:w-[2.828rem]
                            h-[1.168rem]
                            md:h-[1.8rem]
                            lg:h-[2.436rem]
                            opacity-100
                            " :src="value.img" alt="Icon" />
                            <Htag2 class="font-bold w-[5.571rem] md:w-[8.rem] lg:w-[11.616rem] h-[1.5625rem] md:h-[7.5rem] lg:h-12.75" :text="value.title"/>
                            <Ptag class="tracking-normal text-center !w-[5.237rem] md:!w-[7.35rem] lg:!w-[10.92rem]" :text="value.description"/>
                    </div>
                </div>
            </div>
      </div>       
   </section>

</template>