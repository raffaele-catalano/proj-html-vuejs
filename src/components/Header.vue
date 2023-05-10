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
                <div class="dotted-menu_container">
                    <a href="#"><img src="../assets/svg/dotted_menu.svg" alt="dotted-menu"></a> 
                </div>
            </ul>
        </div>
    </div>

</header>
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
                    margin: 0 20px;

                    a {
                        font-weight: 700;
                        font-size: 0.8rem;
                        text-decoration: none;
                        text-transform: uppercase;
                        letter-spacing: .1rem;
                        color: #000000;
                    }
                }
            }
        }
    }
}
</style>