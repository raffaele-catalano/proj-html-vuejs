<script>
import { Swiper, SwiperSlide }  from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import "swiper/css/effect-fade";
import {Pagination, Navigation, Autoplay, EffectFade} from 'swiper';

export default {
    name: 'Jumbotron',
    components: {
        Swiper,
        SwiperSlide
    },
    setup () {
        return {
            modules: [Pagination, Navigation, Autoplay]
        }
    }
}
</script>

<template>
<div class="jumbotron">

    <swiper
        :slidesPerView="1"
        :spaceBetween="0"
        :autoplay="{
        delay: 4000,
        disableOnInteraction: false,
        }"
        :loop="true"
        :pagination="{
            clickable: true,
        }"
        :navigation="true"
        :modules="modules"
        class="mySwiper"
    >
        <swiper-slide class="swiper-core">
            <!-- PRIMA SLIDE -->
            <div class="textual_container">
                <h1>Projects made with <span>love</span></h1>
                <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure debitis molestiae quia et excepturi dignissimos ut beatae blanditiis ab voluptatibus!</p>
                <button class="btn btn-outline-danger btn-warning">Read More</button>
            </div>

            <div class="images_container">
                <img src="../../assets/img/img-Jumbotron/short-slider-rev-1-img-3.png" alt="">
            </div>
        </swiper-slide>

        <!-- SECONDA SLIDE -->
        <swiper-slide class="swiper-core">
            <div class="textual_container">
                <h1>Projects made with <span>love</span></h1>
                <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure debitis molestiae quia et excepturi dignissimos ut beatae blanditiis ab voluptatibus!</p>
                <button class="btn btn-outline-danger btn-warning">Read More</button>
            </div>

            <div class="images_container">
                <img src="../../assets/img/img-Jumbotron/h-2-slider-img-11.png" alt="">
            </div>
        </swiper-slide>

        <!-- TERZA SLIDE -->
        <swiper-slide class="swiper-core">
            <div class="textual_container">
                <h1>Projects made with <span>love</span></h1>
                <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure debitis molestiae quia et excepturi dignissimos ut beatae blanditiis ab voluptatibus!</p>
                <button class="btn btn-outline-danger btn-warning">Read More</button>
            </div>

            <div class="images_container">
                <img src="../../assets/img/img-Jumbotron/h-2-slider-img-15.png" alt="">
                <img src="../../assets/img/img-Jumbotron/h-2-slider-img-16png" alt="">
            </div>
        </swiper-slide>

    </swiper>

</div>
</template>

<style lang="scss" scoped>

.jumbotron {
    .mySwiper {
        width: 100%;
        height: 600px;
        
        .swiper-core {
            widows: 90%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            .textual_container {
                display: flex;
                justify-content: center;
                align-items: center;
                flex-direction: column;
                width: 50%;
                height: 100%;
                //debug
                // border: 1px solid red;

                p {
                    width: 80%;
                }
            }
            .images_container {
                display: flex;
                justify-content: center;
                align-items: center;
                width: 50%;
                height: 100%;
                //debug
                // border: 1px solid blue;
                img{
                    width: 50%;
                }
            }
        }

    }
}

</style>