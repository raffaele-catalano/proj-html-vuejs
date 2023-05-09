<script>
export default {
    name: 'Header'
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
                <li><a href="#">Home</a></li>
                <li><a href="#">Movies</a></li>
                <li><a href="#">TV Series</a></li>
                <li><a href="#">Popular Movies</a></li>
                <li><a href="#">Upcoming</a></li>
            </ul>
            <div class="hamburger-menu_container">
                <a href="#"><img src="../assets/svg/svg-1.svg" alt="hamburger-menu"></a> 
            </div>
        </div>
    </div>

</header>
</template>

<style lang="scss" scoped>
header {
    display: flex;
    justify-content: space-between;
    width: 100vw;
    height: 100px;
    background-color: #FFFFFF;
    // vertical-align: middle;
    //debug
    border: 1px solid limegreen;
    .logo_container{
        display: flex;
        align-items: center;
        margin: 0 0 10px 15px;
        //debug
        // border: 1px solid red;
    }

    .menu_container {
        .nav-bar {
            display: flex;
            align-items: center;
            height: 100%;
            margin-right: 15px;
            .nav-list {
                display: flex;
                align-items: center;
                height: 100%;
                list-style: none;

                li {
                    margin: 0 20px;

                    a {
                        text-decoration: none;
                        text-transform: uppercase;
                        color: #000000;
                    }
                }
            }
            .hamburger-menu_container{
                margin-bottom: 17px;
                //debug
                // border: 1px solid red;
            }
        }
    }
}
</style>