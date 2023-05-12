<script>
import Cards            from './partials/Cards.vue';
import WorkingProcess   from './partials/WorkingProcess.vue';
import Contact          from './partials/Contact.vue';
import Articles         from './partials/Articles.vue';

export default {
    name: 'Main',
    components: {
        Cards,
        WorkingProcess,
        Contact,
        Articles
    }
}
</script>

<template>
    <Cards />
    <WorkingProcess />
    <Contact />
    <Articles />
</template>

<style lang="scss" scoped>

</style>