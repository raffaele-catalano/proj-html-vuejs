<script>
import MainSection1db from '../../data/MainSection-1-db.json'
export default {
    name: 'Cards',
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
        <div class="col p-0" v-for="(card, index) in MainSection1db" :key="index">
            <img :src="`main-first-section-img/${card.src}.jpg`" :alt="card.src">
            <div class="description_container">
                <h3>{{ card.title }}</h3>
                <p>{{ card.description }}</p>
            </div>
        </div>
    </div>
</section>
</template>

<style lang="scss" scoped>

.cards {
    width: 100%;
    .row{
        .col{
            position: relative;
            
            &:hover {
                .description_container{
                    width: 350px;
                    padding: 10px 20px;
                    opacity: 1;

                    h3,
                    p {
                    opacity: 1;
                    }
                }
            }
            //debug
            // border: 2px solid blue;
            .description_container{
                display: flex;
                justify-content: center;
                flex-direction: column;
                position: absolute;
                left: 0;
                top: 50%;
                background-color: white;
                transition: all .6s;
                width: 0;
                height: 100px;
                opacity: 0;
                
                h3,
                p {
                    width: 100%;
                    white-space: nowrap;
                    overflow: hidden;
                    text-overflow: ellipsis;
                    opacity: 0;
                    transition: all .3s;
                }
            }

            img {
                width: 100%;
            }
        }
    }
}

</style>