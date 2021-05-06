<template>
    <div id="my-works">
        <div class="my_works_wrapper">
            <div class="whitespace"></div>
            <div class="art_work_wrapper">
                <div class="art_work">
                    <img class="pic" src="../assets/graphics/idehuset logo.svg" alt="">
                </div>
                <div class="text_control">
                    <h1>Good Shit here</h1>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                        Accusantium autem cum cupiditate dolores ducimus ea enim ipsum, rerum! Ab accusamus.
                    </p>
                    <h2>Stuff1</h2>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta optio, velit rem sit repellat incidunt doloremque, omnis quibusdam consequatur, eligendi nobis. Corrupti ullam rem corporis quisquam, repellat fugiat veritatis blanditiis!
                    </p>
                </div>
            </div>
            <div class="whitespace">
            </div>
            <div class="art_work_wrapper">
                <div class="art_work">
                    <img class="pic" src="../assets/graphics/Esp.png" alt="">
                </div>
                <div class="text_control odd">
                    <h1>Here Here</h1>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                        Accusantium autem cum cupiditate dolores ducimus ea enim ipsum, rerum! Ab accusamus.
                    </p>
                    <h2>SKILLS</h2>
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo vero facere neque hic accusamus tenetur tempore at saepe, beatae nam magni, nesciunt odit esse repellendus! Qui unde molestiae quos tempore.
                    </p>
                </div>
            </div>
             <div class="whitespace">
            </div>
            <div class="video_wrapper">
                <iframe id="myVideo" width="560" height="315" 
                    src="https://www.youtube.com/embed/jnlGWnFtl7s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
                </iframe>
            </div>
             <div class="whitespace">
            </div>
            <div class="art_work_wrapper">
                <div class="art_work">
                    <img class="pic-mini" src="../assets/graphics/mini me.png" alt="">
                </div>
                <div class="text_control">
                    <h1>Heher h1h1</h1>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                        Accusantium autem cum cupiditate dolores ducimus ea enim ipsum, rerum! Ab accusamus.
                    </p>
                    <h2>HEADING NUMBA 2</h2>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus alias, architecto commodi,
                        delectus dignissimos doloribus eaque eius
                        eligendi expedita hic modi nemo.
                    </p>
                </div>
            </div>
            <div class="whitespace">
            </div>
        </div>
        
    </div>
</template>

<script>
    export default {
        name: "MyWorks"
    }
</script>

<style lang="scss" scoped>
    #my-works{
        height:auto;
        width: 100%;
    }

    .my_works_wrapper{
        width:100%;
        height:auto;
        display: flex;
        justify-content: space-around;
        flex-direction: column;
        background-color: #141824;
    }

    .whitespace{
        width:100%;
        height:8rem;
    }

    .art_work_wrapper{
        width: 100%;
        height:25%;
        display: flex;
        justify-content: space-around;
        align-items: center;
        display: flex;
    }

    .art_work_wrapper:nth-child(3n) {
        flex-direction: row-reverse;
    }

    .pic{
        width:350px;
    }

     .pic-mini{
        width:200px;
    }

    .text_control{
        width: 30%;
        height:70%;
    }

     .video_wrapper{
        width:100%;
        height:90vh;
        background-color: #F6F4F2;
        display: flex;
        align-items: flex-end;
        justify-content: center;
    }

    #myVideo{
        width:100%;
        height:100%;
    }

   .art_work {
       padding: 1rem;
   }

    h1{
        font-family: 'Antonio', sans-serif;
        font-family: 'Bebas Neue', cursive;
        font-size: 2.5rem;
        padding: 0;
        color: #0049FF;
        margin: 0;
        margin-top: 10px;
        margin-left: 0rem;
    }

    p{
        font-family: 'Antonio', sans-serif;
        font-family: 'Bebas Neue', cursive;
        opacity: 0.8;
        color: #F6F4F2;
        font-size: 1.2rem;
        font-family: 'Lato', sans-serif;
        font-weight:400;
        padding: 0;
    }

    h2{
    font-family: 'Antonio', sans-serif;
    font-family: 'Bebas Neue', cursive;
    font-size: 2.5rem;
    padding: 0;
    color: #0049FF;
    margin: 0;
    margin-top: 10px;
    margin-left: 0rem;
    }

      @media (max-width: 600px) {
        #my-works{
            height: auto;
        }

        .whitespace{
            height:5px;
        }

        .art_work_wrapper{
            width:100%;
            height:100%;
            padding: 2rem;
            display: flex;
            justify-content:flex-start;
            align-items: center;
            flex-direction: column;
        }

        .art-work{
            flex-direction: column;
            height:25%;
        }

        .art_work:nth-child(3n) {
            flex-direction: column;
        }

        img{
            width:300px;
        }

        .text_control{
            width: 80%;
            height:30%;
            transform: translate(0px, 0px);
        }

        h1{
            font-size: 24px;
        }

        p{
            font-size: 16px;
        }

        h2{
                  font-size: 24px;
        }

    }

</style>
