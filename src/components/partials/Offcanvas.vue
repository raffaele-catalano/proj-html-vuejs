<script>
export default {
    name: 'Offcanvas'
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
        <div class="textual_info w-75">
            <p class="text-center">This is Marée, a colorful new portfolio for presenting your work. If you’re a modern illustrator or a designer, we made Marée for you.</p>
        </div>
        <!-- div social da ciclare dinamicamente -->
        <div class="social_container">
            <p>T P F L</p>
        </div>

    </div>
</div>
</template>

<style lang="scss" scoped>

</style>