<script>
import SocialDb from '../data/Social-db.json'
export default {
    name: 'Footer',
    data(){
        return {
            SocialDb
        }
    },
    methods: {
        scrollToTop() {
            window-scrollTo ({
                top: 0,
            })
        }
    }
}
</script>

<template>
    <footer>
        <div class="footer_container">
            <div class="logo_container">
                <img src="../assets/img/logo-sidearea-1.png" alt="logo">
            </div>

            <div class="info_container">

                <div class="row row-cols-3">

                    <div class="col">
                        <p>maree@qodeinteractive.com</p>
                        <p>+44 645 321 789</p>
                    </div>
                    <div class="col">
                        <p>Avenue d'Auderghem 10</p>
                        <p>1040 Brussels, Belgium</p>
                    </div>
                    <div class="col">
                        <p>Stay in touch with us</p>
                        <div class="icons_container">
                            <i :class="icon.icon" v-for="(icon, index) in SocialDb" :key="index"></i>
                        </div>
                    </div>

                </div>
            </div>
        </div>
        <div class="pageUp_container">
            <a href="#" @click="scrollToTop">
                <img src="../assets/svg/arrow-up.svg" alt="arrow-up">
            </a>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    display: flex;
    justify-content: center;
    background-color: #C0E1CF;
    width: 100%;
    height: 230px;
    // margin-bottom: 20px;
    .footer_container {
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 100%;
        width: 80%;
        //debug
        // border: 1px solid red;
        .logo_container {
            width: 30%;
            
        }

        .info_container {
            width: 60%;
            height: 100%;
            //debug
            // border: 1px solid black;
            .row {
                display: flex;
                justify-content: center;
                align-items: center;
                width: 100%;
                height: 100%;
                //debug
                // border: 1px solid gold;
                .col {
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    height: 100%;
                    //debug
                    // border: 1px solid red;
                    
                    &:last-of-type {
                        margin-bottom: 15px;
                        //debug
                        // background-color: lightcoral;
                    }
                    .icons_container{
                        //debug
                        // border: 1px solid red;
                        i {
                            margin: 0 15px;
                            font-size: 1.1rem;
                            cursor: pointer;
                            transition: all .3s;

                            &:hover {
                                transform: scale(1.2);
                                color: white;
                            }
                        }
                    }
                }
            }
        }
    }
    .pageUp_container {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 10%;
        //debug
        // border: 1px solid black;
        
        a {
            cursor: pointer;
            padding: 10px;
            transition: all .5s;
            // debug
            // border: 1px solid red;
            &:hover {
                background-color: #F4CFC7;
                border-radius: 50%;
            }

            img {
                padding-right: 5px;
                width: 120%;
            }
            
        }
    }
}
</style>