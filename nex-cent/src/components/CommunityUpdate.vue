<script setup>
import communitUpdateImg1 from '../assets/communityUpdate1.jpg'
import communitUpdateImg2 from '../assets/communityUpdate2.jpg'
import communitUpdateImg3 from '../assets/communityUpdate3.jpg'
import Ptag from './Ptag.vue'
import Htag2 from './Htag2.vue'

const communitUpdateData=[
    {
        img: communitUpdateImg1,
        description: 'Creating Streamlined Safeguarding Processes with OneRen'
    },
    {
        img: communitUpdateImg2,
        description: 'What are your safeguarding responsibilities and how can you manage them?'
    },
    {
        img: communitUpdateImg3,
        description: 'Revamping the Membership Model with Triathlon Australia'
    },
]
const pTagText = 'The Nextcent blog is the best place to read about the latest membership insights, trends and more. See who\'s joining the community, read about how our community are increasing their membership income and lot\'s more.​';
</script>

<template>

    <section class=" flex flex-col justify-center items-center mt-5 ">
        <div class="flex flex-col justify-center items-center gap-5">
            <Htag2 class=" w-[23.162rem] md:w-[34.264rem] lg:w-[48.289rem] h-[0.914rem] md:h-1.25 lg:h-7.75" :text="'Caring is the new marketing'"/>
            <Ptag class="trackin-normal text-center !w-[13.790rem] md:!w-[20.625rem] lg:!w-[27.321rem] " :text="pTagText"/>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-5 ">
                <div class="relative flex flex-col justify-center items-center w-[7.679rem] md:w-[11.324rem] lg:w-[16.009rem] h-[7.679rem] md:h-[11.324rem] lg:h-[15.987rem] opacity-100" v-for="value in communitUpdateData" :key="value.description">
                    <img :src="value.img" alt="">
                    <div class="absolute -bottom-5 flex flex-col justify-center items-center
                        w-[6.696rem]
                        md:w-[10.034rem]
                        lg:w-[13.790rem]
                        h-[3.478rem]
                        md:h-[5.208rem]
                        lg:h-[7.722rem]
                        gap-[0.348rem]
                        md:gap-[0.522rem]
                        lg:gap-[0.696rem]
                        p-[0.348rem]
                        md:p-[0.522rem]
                        lg:p-[0.696rem]
                        rounded-[0.174rem]
                        md:rounded-[0.262rem]
                        lg:rounded-[0.348rem]
                        bg-[#F5F7FA]
                        shadow-[0_0.348rem_0.696rem_0_#ABBED166]
                        opacity-100
                        ">
                        <Ptag class="font-semibold tracking-normal text-center !w-[5.938rem] md:!w-[8.912rem] lg:!w-[12.398rem] " :text="value.description"/>
                        <button class="
                            font-inter
                            font-semibold
                            text-[0.418rem]
                            md:text-[0.42rem]
                            lg:text-[0.87rem]
                            leading-[0.588rem]
                            md:leading-[0.936rem]
                            lg:leading-[1.218rem]
                            tracking-normal
                            align-middle
                            text-[#4CAF4F]
                            w-[2.9625rem]
                            md:w-17.125
                            lg:w-24.25
                            h-[0.625rem]
                            md:h-3
                            lg:h-5
                            opacity-100
                            ">Read More... →
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>