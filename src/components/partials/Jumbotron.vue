<script>
import { Swiper, SwiperSlide }  from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import {Pagination, Navigation} from 'swiper';

export default {
    name: 'Jumbotron',
    components: {
        Swiper,
        SwiperSlide
    },
    setup () {
        return {
            modules: [Pagination, Navigation]
        }
    }
}
</script>

<template>
<div class="jumbotron">

    <swiper
        :slidesPerView="1"
        :spaceBetween="30"
        :loop="true"
        :pagination="{
            clickable: true,
        }"
        :navigation="true"
        :modules="modules"
        class="mySwiper"
    >
        <swiper-slide>Slide 1</swiper-slide>
        <swiper-slide>Slide 2</swiper-slide>
    </swiper>

</div>
</template>

<style lang="scss" scoped>

.jumbotron {
    .mySwiper {
        width: 100%;
        height: 600px;
    }
}

</style>