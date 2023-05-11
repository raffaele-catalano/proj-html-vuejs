<script>
import { Swiper, SwiperSlide }  from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import "swiper/css/effect-fade";
import {Pagination, Navigation, Autoplay} from 'swiper';

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
                <h1 class="text-center">Projects made with <span class="different_font">love</span></h1>
                <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure debitis molestiae quia et excepturi dignissimos ut beatae blanditiis ab voluptatibus!</p>
                <button type="button" class="btn">Read More</button>
            </div>

            <div class="images_container">
                <img src="../../assets/img/img-Jumbotron/short-slider-rev-1-img-3.png" alt="">
            </div>
        </swiper-slide>

        <!-- SECONDA SLIDE -->
        <swiper-slide class="swiper-core">
            <div class="textual_container">
                <h1 class="text-center">Our new folio full of <span class="different_font">joy</span></h1>
                <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure debitis molestiae quia et excepturi dignissimos ut beatae blanditiis ab voluptatibus!</p>
                <button type="button" class="btn">Read More</button>
            </div>

            <div class="images_container">
                <img src="../../assets/img/img-Jumbotron/h-2-slider-img-11.png" alt="">
            </div>
        </swiper-slide>

        <!-- TERZA SLIDE -->
        <swiper-slide class="swiper-core">
            <div class="textual_container">
                <h1 class="text-center">Devotion that never <span class="different_font">ends</span></h1>
                <p class="text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure debitis molestiae quia et excepturi dignissimos ut beatae blanditiis ab voluptatibus!</p>
                <button type="button" class="btn">Read More</button>
            </div>

            <div class="images_container_double">
                <img src="../../assets/img/img-Jumbotron/h-2-slider-img-15.png" alt="">
                <img src="../../assets/img/img-Jumbotron/h-2-slider-img-16.png" alt="">
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
            .images_container_double {
                img {
                    width: 50%;
                }
            }

            &:nth-child(2) {
                .images_container {
                    img {
                        width: 80%;
                    }
                }
            }
        }

    }
}

</style>