<script>
export default {
    name: 'Card',
    props: {
        Image       : String,
        Title       : String,
        Description : String
    }
}
</script>

<template>
<div class="col p-0">
    <img :src="`/main-first-section-img/${Image}.jpg`" :alt="Image">
    <div class="description_container">
        <h3>{{ Title }}</h3>
        <p>{{ Description }}</p>
    </div>
</div>
</template>

<style lang="scss" scoped>
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
                p {
                    font-style: italic;
                    font-family: "Playfair Display", serif !important;
                }
            }

            img {
                width: 100%;
            }
        }
</style>