<script>
export default {
    name: 'Articles',
}
</script>

<template>
    <section>
        <div class="articles_container">
            <div class="row row-cols-3">

                <div class="col article">

                    <div class="bookmark_container">
                        <div class="day">
                            <h3>12</h3>
                        </div>
                        <div class="month-year">
                            <p class="text-uppercase">may '23</p>
                        </div>
                    </div>

                    <div class="article_thumb overflow-hidden">
                        <img src="../../assets/img/img-Main/main-last-section/h-2-blog-img-1.jpg" alt="">
                    </div>

                    <h4 class="text-capitalize my-3">this way, love: a detailed guide through new design</h4>
                    <p class="author text-capitalize">by emily fields</p>
                </div>
                
                <div class="col article">

                    <div class="bookmark_container">
                        <div class="day">
                            <h3>12</h3>
                        </div>
                        <div class="month-year">
                            <p class="text-uppercase">may '23</p>
                        </div>
                    </div>

                    <div class="article_thumb overflow-hidden">
                        <img src="../../assets/img/img-Main/main-last-section/h-2-blog-img-2.jpg" alt="">
                    </div>
                    <h4 class="text-capitalize my-3">i try to give people a different way of looking art</h4>
                    <p class="author text-capitalize">by emily fields</p>
                </div>

                <div class="col article">

                    <div class="bookmark_container">
                        <div class="day">
                            <h3>12</h3>
                        </div>
                        <div class="month-year">
                            <p class="text-uppercase">may '23</p>
                        </div>
                    </div>

                    <div class="article_thumb overflow-hidden">
                        <img src="../../assets/img/img-Main/main-last-section/h-2-blog-img-3.jpg" alt="">
                    </div>
                    <h4 class="text-capitalize my-3">introduce richard laperrière of those amazing features</h4>
                    <p class="author text-capitalize">by emily fields</p>
                </div>

            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

section {
    height: 700px;
    .articles_container {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100%;
        .row {
            width: 70%;
            .col {
                position: relative;
                .bookmark_container {
                    display: flex;
                    flex-direction: column;
                    position: absolute;
                    z-index: 15;
                    top: -15px;
                    left: 20px;
                    width: 70px;
                    height: 80px;
                    box-shadow: 0 0 10px rgba($color: #000000, $alpha: .2);
                    .day {
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        width: 100%;
                        height: 55%;
                        background-color: #C0E1CF;
                        //debug
                        // border: 1px solid red;
                        h3 {
                            text-align: center;
                            font-family: "Playfair Display", serif !important;
                            font-style: italic;
                            font-weight: 800;
                            font-size: 2.3rem;
                            //debug
                            // border: 1px solid blue;
                        }
                    }
                    .month-year{
                        width: 100%;
                        height: 45%;
                        background-color: #F3D0C7;
                        //debug 
                        // border: 1px solid blue;
                        p {
                            text-align: center;
                            padding-top: 7px;
                            font-weight: 700;
                            font-size: 0.7rem;
                            letter-spacing: .1rem;
                        }
                    }
                }
                img {
                    width: 100%;
                    transition: all .5s;

                    &:hover {
                        transform: scale(1.03);
                        cursor: pointer;
                    }
                }
                h4 {
                    font-size: 1.5rem;
                }
                .author {
                    font-family: "Playfair Display", serif !important;
                    font-style: italic;
                }
            }
        }
    }
}

</style>