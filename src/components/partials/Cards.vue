<script>
import MainSection1db from '../../data/MainSection-1-db.json'
import Card from '../partials/micro-components/Card.vue'
export default {
    name: 'Cards',
    components: {
        Card
    },
    data() {
        return {
            MainSection1db,
        }
    }
}
</script>

<template>
    <section class="cards">
        <div class="row row-cols-3">
            <Card v-for="(card, index) in MainSection1db" :key="index" :Image="card.src" :Title="card.title" :Description="card.description" />
        </div>
    </section>
</template>

<style lang="scss" scoped>

.cards {
    width: 100%;
}

</style>