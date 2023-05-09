<script>
export default {
    name: 'WorkingProcess',
}
</script>

<template>
<section class="working-process">

    <div class="wrapper">

        <div class="title_container mb-4">
            <h1 class="text-center">Working <span class="process"><em>process</em></span></h1>
        </div>

        <div class="graph_container">

            <div class="process-container">
                <div class="rounded_container my-2">
                    <i class="fa-solid fa-lightbulb fa-flip-horizontal fa-2xl" style="color: #BADAC9"></i>
                </div>
                <h5>First theres an idea</h5>
                <p class="text-center">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Fuga labore maiores nostrum fugit?</p>
            </div>
            
            <div class="process-container">
                <div class="rounded_container my-2">
                    <i class="fa-regular fa-comment fa-2xl" style="color: gold"></i>
                </div>
                <h5>Then we talk about</h5>
                <p class="text-center">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Fuga labore maiores nostrum fugit?</p>
            </div>

            <div class="process-container">
                <div class="rounded_container my-2">
                    <i class="fa-solid fa-cloud fa-2xl" style="color: #80465F"></i>
                </div>
                <h5>And we think about</h5>
                <p class="text-center">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Fuga labore maiores nostrum fugit?</p>
            </div>

            <div class="process-container">
                <div class="rounded_container my-2">
                    <i class="fa-solid fa-pencil fa-2xl" style="color: #EB6950"></i>
                </div>
                <h5>So we draw along</h5>
                <p class="text-center">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Fuga labore maiores nostrum fugit?</p>
            </div>

        </div>

    </div>

</section>
</template>

<style lang="scss" scoped>

.working-process {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 700px;
    //debug
    // background-color: lightcyan;
    .wrapper {
        display: flex;
        flex-direction: column;
        width: 70%;
        //debug 
        // border: 1px solid blue;
        // background-color: lightsalmon;
        .title_container{
            width: 100%;
            //debug
            // border: 1px solid lime;
    
            h1 {
                font-size: 3.5rem;
            }
            .process {
                font-weight: 700;
                
            }
        }

        .graph_container {
            display: flex;
            width: 100%;
            gap: 1rem;
            background-image: url(../../assets/svg/wave_line.svg);
            background-repeat: no-repeat;
            background-position:top;
            //debug 
            // border: 1px solid red;
            .process-container {
                display: flex;
                flex-direction: column;
                align-items: center;
                //debug
                // border: 1px solid blue;
                p {
                    color: gray;
                }

                .rounded_container {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    width: 150px;
                    height: 150px;
                    background-color: #FAF7F1;
                    border-radius: 50%;
                    //debug
                    // border: 1px solid red;
                    i {
                        font-size: 3rem;
                    }
                }
            }
        }
    }
}

</style>