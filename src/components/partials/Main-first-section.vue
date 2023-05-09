<script>
export default {
    name: 'Cards',
}
</script>

<template>
<section class="cards">
    <div class="row row-cols-3">
        <div class="col p-0">
            <img src="../../assets/img/img-Main/main-first-section/img-1.jpg" alt="">
        </div>
        <div class="col p-0">
            <img src="../../assets/img/img-Main/main-first-section/img-2.jpg" alt="">
        </div>
        <div class="col p-0">
            <img src="../../assets/img/img-Main/main-first-section/img-3.jpg" alt="">
        </div>
        <div class="col p-0">
            <img src="../../assets/img/img-Main/main-first-section/img-4.jpg" alt="">
        </div>
        <div class="col p-0">
            <img src="../../assets/img/img-Main/main-first-section/img-5.jpg" alt="">
        </div>
        <div class="col p-0">
            <img src="../../assets/img/img-Main/main-first-section/img-6.jpg" alt="">
        </div>
    </div>
</section>
</template>

<style lang="scss" scoped>
@use "../../scss/main.scss" as *;
@use "../../scss/partials/typography" as *;

.cards {
    width: 100%;
    .row{
        .col{
            //debug
            // border: 2px solid blue;
            img {
                width: 100%;
                object-fit: contain;
            }
        }
    }
}

</style>