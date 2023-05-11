<script>
import { menuHeader } from '../data/database';
import Jumbotron      from './partials/Jumbotron.vue';
import Offcanvas      from './partials/Offcanvas.vue';

export default {
    name: 'Header',
    components: {
        Jumbotron,
        Offcanvas
    },
    data (){
        return {
            menuHeader,
            dropdownOpen: false,
        }
    }
}
</script>

<template>
<header>

    <div class="logo_container">
        <img src="../assets/img/logo-sidearea-1.png" alt="main-logo">
    </div>

    <div class="menu_container">
        <div class="nav-bar">

            <ul class="nav-list">

                <li class="position-relative" v-for="(menuItem, index) in menuHeader" :key="index" @mouseenter="dropdownOpen = true" @mouseleave="dropdownOpen = false">
                    <a href="#">{{ menuItem.label }}</a>
                    <!-- inizio dropdown menu -->
                    <div class="dropdown_menu position-absolute" v-if="menuItem.dropDown">
                        <ul class="list-unstyled">
                            <li v-for="dropdownItem in menuItem.dropDown" :key="dropdownItem"> {{ dropdownItem }}</li>
                        </ul>
                    </div>

                    <div class="dropdown_menu position-absolute megamenu" v-if="menuItem.dropDownList">
                        <ul class="list-unstyled d-flex">
                            <li v-for="dropdownItem in menuItem.dropDownList" :key="dropdownItem"> 

                                <ul class="list-unstyled">
                                    <li> 
                                        <span class="fw-bold text-uppercase">{{ dropdownItem.label }}</span>
                                        
                                    </li>

                                    <li class="megamenu_list" v-for="link in dropdownItem.links" :key="link"> 
                                        <span>{{ link }}</span>
                                    </li>
                                </ul>

                            </li>
                        </ul>
                    </div>

                </li>
                <div class="dotted-menu_container">
                    <a href="#offcanvas" data-bs-toggle="offcanvas" role="button" aria-controls="offcanvas"><img src="../assets/svg/dotted_menu.svg" alt="dotted-menu"></a> 
                    <!-- OFFCANVAS -->
                    <Offcanvas />
                </div>
            </ul>
        </div>
    </div>
</header>
<!-- JUMBOTRON -->
<Jumbotron />
</template>

<style lang="scss" scoped>

header {
    display: flex;
    justify-content: space-between;
    width: 100%;
    height: 100px;
    background-color: #FFFFFF;
    box-shadow: 0 0 10px rgba($color: #000000, $alpha: 0.2);
    //debug
    // border-bottom: 1px solid limegreen;
    .logo_container{
        display: flex;
        align-items: center;
        margin-left: 15px;
        //debug
        // border: 1px solid red;
    }

    .menu_container {
        height: 100px;
        .nav-bar {
            display: flex;
            height: 100%;
            margin-right: 15px;
            .nav-list {
                display: flex;
                align-items: center;
                height: 100%;
                list-style: none;
                gap: 1.5rem;
                //debug
                // border: 1px solid red;
                
                
                li {
                    width: 100%;
                    height: 100%;
                    display: flex;
                    align-items: center;
                    margin: 0 20px;
                    
                    &:hover {
                        .dropdown_menu{
                            display: block;
                        }
                    }
                    
                    a {
                        font-weight: 700;
                        font-size: 0.8rem;
                        text-decoration: none;
                        text-transform: uppercase;
                        letter-spacing: .1rem;
                        color: #000000;
                    }
                    
                    .dropdown_menu {
                        display: none;
                        top: 100%;
                        min-width: 200px;
                        background-color: #FCFAF6;
                        z-index: 500;
                        overflow: hidden;
                        transition: all .4s;

                        ul {
                            li{
                                padding: 8px 0;
                            }
                        }
                    }

                    .dropdown_menu.megamenu{
                        .megamenu_list{
                            min-width: 200px;

                            span {
                                color: gray;
                            }
                        }
                    }
                }
            }
        }
    }
}
</style>