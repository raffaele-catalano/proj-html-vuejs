<script>
import { Swiper, SwiperSlide }  from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import "swiper/css/effect-fade";
import {Pagination, Navigation, Autoplay, EffectFade} from 'swiper';

import JumboDb from "../../data/Jumbo-db.json"

export default {
    name: 'Jumbotron',
    components: {
        Swiper,
        SwiperSlide
    },
    data () {
        return {
            JumboDb
        }
    },
    setup () {
        return {
            modules: [Pagination, Navigation, Autoplay, EffectFade]
        }
    },
    methods: {
        getImage(img){
            return new URL(img, import.meta.url).href;
        }
    }
}
</script>

<template>
<div class="jumbotron">

    <swiper
        :slidesPerView="1"
        :spaceBetween="0"
        :effect="'fade'"
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
        <swiper-slide class="swiper-core" v-for="(slide, index) in JumboDb" :key="index">
            <!-- PRIMA SLIDE -->
            <div class="textual_container">
                <h1 class="text-center"> {{ slide.title }} <span class="different_font">{{ slide.italic }}</span></h1>
                <p class="text-center">{{ slide.description }}</p>
                <button type="button" class="btn">{{ slide.button }}</button>
            </div>

            <div class="images_container" :class="{'double': slide.image2 != ''}">
                <img :src="getImage(`../../assets/img/img-Jumbotron/${slide.image}`)" alt="">
                <img v-if="slide.image2 != ''" :src="getImage(`../../assets/img/img-Jumbotron/${slide.image2}`)" alt="">
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
            justify-content: flex-end;
            align-items: center;
            background-color: white;
            position: relative;
            .textual_container {
                display: flex;
                justify-content: center;
                align-items: center;
                flex-direction: column;
                width: 50%;
                height: 100%;
                position: absolute;
                left: 0;
                top: 0;
                //debug
                // border: 1px solid red;
                h1 {
                    font-size: 5rem;
                    width: 70%;
                }
                .different_font{
                    font-weight: 900;
                    font-style: italic;
                    font-family: "Playfair Display", serif !important;
                }

                p {
                    width: 70%;
                    font-size: 1.2rem;
                    color: gray;
                }
                .btn {
                    padding: 15px 40px;
                    font-weight: 700;
                    font-size: 0.9rem;
                    text-transform: uppercase;
                    letter-spacing: .1rem;
                    border: 2px solid #E1C0B0;
                    transition: all .4s;

                    &:hover {
                        background-color: #E1C0B0;
                        color: white;
                    }
                }
            }
            .images_container {
                display: flex;
                align-items: center;
                width: 50%;
                height: 100%;
                //debug
                // border: 1px solid blue;
                img{
                    width: 80%;
                    height: 80%;
                    object-fit: contain;
                }
            }
            .images_container.double {
                img {
                    width: 40%;
                    height: 80%;
                    object-fit: contain;
                }
            }

            &:nth-child(2) {
                .images_container {
                    #jumbo_image {
                        width: 85%;
                    }
                }
            }
        }

    }
}

</style>