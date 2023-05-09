<script>
import Cards            from './partials/Main-section-1.vue';
import WorkingProcess   from './partials/Main-section-2.vue'
import Contact          from './partials/Main-section-3.vue'

export default {
    name: 'Main',
    components: {
        Cards,
        WorkingProcess,
        Contact,
    }
}
</script>

<template>
<Cards />
<WorkingProcess />
<Contact />
</template>

<style lang="scss" scoped>

</style>