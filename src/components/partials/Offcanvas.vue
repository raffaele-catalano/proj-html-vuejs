<script>
import SocialDb from '../../data/Social-db.json'

export default {
    name: 'Offcanvas',
    data() {
        return {
            SocialDb
        }
    }
}
</script>

<template>
    <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvas" aria-labelledby="offcanvasLabel">
        <div class="offcanvas-header d-flex justify-content-end">
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body d-flex align-items-center flex-column">
            <div class="logo_container mb-3">
                <img src="../../assets/img/logo-sidearea-1.png" alt="logo">
            </div>
            <div class="textual_info w-75 mb-3">
                <p class="text-center">This is Marée, a colorful new portfolio for presenting your work. If you’re a modern illustrator or a designer, we made Marée for you.</p>
            </div>
            <div class="icons_container">
                <i :class="icon.icon" v-for="(icon, index) in SocialDb" :key="index"></i>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.textual_info {
    p {
        color: gray;
    }
}
.icons_container {
    i {
        cursor: pointer;
        padding: 10px 10px;
        font-size: 1.2rem;
        transition: all .3s;

        &:hover {
            transform: scale(1.3);
            color: #a0e7bf;
        }
    }
}
</style>