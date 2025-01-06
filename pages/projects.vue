<template>
    <div class="mx-auto py-5 px-4">
        <div class="bg-primary border-4 rounded-[40px] p-5 border-[#d7a947] text-white">
            <h2 data-aos="zoom-in" class=" abril-fatface-regular-font text-5xl md:text-6xl uppercase text-center">My Projects</h2>
            <!-- <div class="mt-5">
                <h2 class="text-center text-2xl">Pending...</h2>
            </div> -->


            <a-carousel arrows>
                <template #prevArrow>
                    <div class="custom-slick-arrow" style="left: 10px; z-index: 1">
                        <!-- <left-circle-outlined /> -->
                        <LeftOutlined />
                    </div>
                </template>
                <template #nextArrow>
                    <div class="custom-slick-arrow" style="right: 10px">
                        <!-- <right-circle-outlined /> -->
                        <RightOutlined />
                    </div>
                </template>
                <CAM/>
                <DTEC/>
                <LittleReportersClub/>
                <XanhThienNguyen/>
                <YEMUN/>
            </a-carousel>

        </div>
    </div>
</template>

<script setup lang="ts">
import { LeftOutlined, RightOutlined } from '@ant-design/icons-vue';
import CAM from '~/components/projects/CAM.vue';
import DTEC from '~/components/projects/DTEC.vue';
import LittleReportersClub from '~/components/projects/LittleReportersClub.vue';
import XanhThienNguyen from '~/components/projects/XanhThienNguyen.vue';
import YEMUN from '~/components/projects/YEMUN.vue';
</script>

<style scoped>
/* For demo */
:deep(.slick-slide) {
    /* text-align: center; */
    /* height: 160px; */
    /* line-height: 160px; */
    /* background: #364d79; */
    overflow: hidden;
}

:deep(.slick-arrow.custom-slick-arrow) {
    margin-right: -150px;
    margin-left: -150px;
    width: 50px;
    height: 50px;
    font-size: 50px;
    color: #d7a947;
    /* background-color: rgba(31, 45, 61, 0.11); */
    transition: ease all 0.3s;
    /* opacity: 0.3; */
    z-index: 1;
}

:deep(.slick-arrow.custom-slick-arrow:before) {
    display: none;
}

:deep(.slick-arrow.custom-slick-arrow:hover) {
    color: #710014;
    /* opacity: 0.5; */
}

/* :deep(.slick-slide h3) {
    color: #fff;
} */
</style>