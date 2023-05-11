<script>
export default {
    name: 'Contact',
}
</script>

<template>
<section>
    <div class="contact_container">

        <h2>Want to work with us? Send us <span class="a-message">a message!</span></h2>

        <p class="text-center">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Placeat, odio eos quod ea, quasi animi necessitatibus ullam est ab, neque similique nesciunt dolores autem? Nihil alias eum quam sapiente at!
        </p>

        <button type="button" class="btn text-uppercase">contact</button>
    </div>
</section>
</template>

<style lang="scss" scoped>

section {
    display: flex;
    justify-content: center;
    width: 100%;
    height: 530px;
    background-image: url(../../assets/img/h-2-background-1.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    box-shadow: 0 0 10px rgba($color: #000000, $alpha: 0.1);
    //debug
    // border: 1px solid black;
    margin-bottom: 50px;
    .contact_container{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        width: 70%;
        height: 100%;
        //debug
        // border: 1px solid red;

        h2 {
            font-size: 4rem;
            margin-bottom: 20px;
            margin-top: 5px;
            .a-message {
                font-weight: 900;
                font-style: italic;
                font-family: "Playfair Display", serif !important;
            }
        }
        p {
            color: gray;
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        .btn{
            background-color: #D8F0E3;
            font-weight: 700;
            font-size: 0.8rem;
            letter-spacing: .2rem;
            padding: 16px 60px;
            transition: all .3s;

            &:hover {
                background-color: #F2D0C7;
                color: white;
            }
        }
    }
}

</style>