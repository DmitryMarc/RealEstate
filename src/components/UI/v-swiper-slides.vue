<template>
    <swiper
        :modules="modules" 
        :slides-per-view="1" 
        :navigation="{
            prevEl: '#swiper-prev',
            nextEl: '#swiper-next'
        }" 
    >
        <swiper-slide
            v-for="item in totalPages"
            :key="item"
        >
            <slot></slot>
        </swiper-slide>
    </swiper>
</template>

<script>
import { Navigation } from 'swiper/modules';
import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

export default {
    props:{
        totalPages: Number
    },
    components: {
        Swiper,
        SwiperSlide
    },
    setup() {
        const onSwiper = (swiper) => {
            console.log(swiper);
        };
        const onSlideChange = () => {
            console.log('slide change');
        };
        return {
            onSwiper,
            onSlideChange,
            modules: [Navigation],
        };
    },
}

</script>