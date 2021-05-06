<template>
  <div class="container">
      <div class="header-wrapper">
          <div class="mini-me-wrapper">
            <img class="mini-me-banner" src="../assets/graphics/mini me.png" alt="">
          </div>
          <div class="heading-text-banner">
            <div class="text-wrapper">
              <span class="header-heading">Claus Feldberg</span>
              <span class="header-heading">Portfolio.</span>
            </div>
          </div>
      </div>
       <div id="about-me" class="video_wrapper">
          <iframe  id="myVideo" width="560" height="315" src="https://www.youtube.com/embed/tZ7OPH0PZfE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      <div class="second-section">
        <div class="icons-wrapper">
            <div class="icon-container">
                <i class="fas flex-ico fa-handshake"></i>
                  <p class="section-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil in culpa deleniti ipsam. </p>
            </div>
              <div class="icon-container">
                <i class="fas fa-grin-hearts flex-ico "></i>
                  <p class="section-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil in culpa deleniti ipsam.</p>
            </div>
              <div class="icon-container">
                <i class="far flex-ico fa-object-ungroup"></i>
                  <p class="section-text">hashfjaskjasbi </p>
            </div>
        </div>
      </div>
      <v-parallax height="750" src="../assets/pics/miig.jpg">
        <div class="parallax-wrapper">
          <div class="first-section-wrapper">
            <h2 class="section-heading">Lorem ipsum</h2>
            <div class="circular-banner">
            </div>
            <p class="section-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil in culpa deleniti ipsam. Magnam earum officiis at quos veniam dicta porro nulla amet quibusdam? Aliquid facere cum cupiditate earum neque.</p>
        </div>
        </div>
      </v-parallax>
      <MyWorks></MyWorks>
      <div class="my-photos-wrapper">
          <i class="fas camera-ico fa-camera-retro"></i>
          <span class="my-photos-banner"> My photos </span>
      </div>
    <v-carousel height="700" :show-arrows="true">
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
      ></v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
import MyWorks from "../components/MyWorks"

  export default {
    name: 'Home',

      components: {
            MyWorks
        },

        data () {
            return {
                drawer: false,
                items: [
                    {
                        src: require ('../assets/pics/fish-eye.jpg'),
                    },
                    {
                        src: require ('../assets/pics/skate-pa-havn.jpg'),
                    },
                    {
                        src: require ('../assets/pics/land-scape.jpg'),
                    },
                    {
                        src: require ('../assets/pics/havn.jpg'),
                    },
                    {
                        src: require ('../assets/pics/homies.jpeg'),
                    },
                    {
                        src: require ('../assets/pics/river.jpeg'),
                    },
                    {
                        src: require ('../assets/pics/sea.jpeg'),
                    },
                ],
            }
        },
  }
</script>

<style  scoped>
.container {
    perspective: 1px;
    height: auto;
    display: flex;
    flex-direction: column;
    perspective: 1px;
    transform-style: preserve-3d;
    overflow-y: scroll;
    overflow-x: hidden;
   
}
  .header-wrapper {
    width: 100%;
    height: 70vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #F6F4F2;
    display: flex;
    
  }

  .mini-me-wrapper {
    width: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .mini-me-banner {
    width: 11rem;
  }

  .heading-text-banner {
    width: 50%;
    display: flex;
    align-items: center;
    background-color: #141824;
    border-bottom-left-radius: 5px;
    border-top-left-radius: 5px;
    box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
    padding: 2rem;
    height: auto;
    justify-content: flex-start;
  }

  .my-photos-wrapper {
    width: 100%;
    height: 40vh;
    background-color: #0049FF;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
    padding-bottom: 3rem;
  }

  .camera-ico {
    color:#141824;
    font-size: 4.5rem;
    margin-bottom: 1rem;
  }

  .my-photos-banner {
     font-family: 'Antonio', sans-serif;
    font-family: 'Bebas Neue', cursive;
    font-size: 3.5rem;
    padding: 0;
    color: whitesmoke;
    margin: 0;
    margin-left: 0rem;
  }

  .header-heading {
    font-family: 'Antonio', sans-serif;
    font-family: 'Bebas Neue', cursive;
    font-size: 5rem;
    padding: 0;
    color: #F6F4F2;
    margin: 0;
    margin-left: 3rem;
  }

  .circular-banner {
    width: 1.5rem;
    height: 1.5rem;
    background-color: #0049FF;
    border-radius: 25px;
    margin-bottom: 1.5rem;
  }

  .text-wrapper {
    display: flex;
    height: auto;
    flex-direction: column;
    justify-content: flex-start;

  }

  .header-heading:last-child{
    color: #0049FF;
  }

  .parallax-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
    padding: 0;
    margin: 0;
    background:rgba(0,0,0,0.6);
  }

  .first-section-wrapper {
    width: 45%;
    padding: 5rem;
    height: auto;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    border-radius: 10px;
  }

  .section-heading {
    font-family: 'Antonio', sans-serif;
    font-family: 'Bebas Neue', cursive;
    font-size: 3.5rem;
    padding: 0;
    color: #0049FF;
    margin: 0;
    margin-left: 0rem;
  }

  .section-text {
    font-family: 'Antonio', sans-serif;
    font-family: 'Bebas Neue', cursive;
    color: #F6F4F2;
    font-size: 1.2rem;
    font-family: 'Lato', sans-serif;
    font-weight:400;
    padding: 0;
  }

  .second-section {
    width: 100%;
    height: 55vh;
    background-color: #0049FF;
    opacity: 0.95;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }

  .icons-wrapper {
    display: flex;
    max-width: 70%;
    align-items: center;
    justify-content: space-between;
  }

  .icon-container {
    width: 30%;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    text-align: center;
  }

  .flex-ico {
    font-size: 6.5rem;
    color: #141824;
    margin-bottom: 1rem;
  }

  .triangular-shaper {
    width: 100%;
    height: 20rem;
    clip-path: polygon(50% 31%, 0 0, 100% 0);
    background-color: #0049FF;
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

    @media (max-width: 600px) {
      .first-section-wrapper {
        width: 100%;
        text-align: center;
      } 
        .header-wrapper {
          height: auto;
          padding: 2rem;
          flex-direction: column;
      }

      .parallax-wrapper {
        width: 100%;
      }

      .icon-container {
        width: 100%;
        margin-bottom: 2rem;
      }

       .header-heading {
    font-family: 'Antonio', sans-serif;
    font-family: 'Bebas Neue', cursive;
    font-size: 4.5rem;
    padding: 0;
    color: #141824;
    margin: 0;
  }

  .icons-wrapper {
    flex-direction: column; 
    height: auto;
      width: 100%;
  }

    .second-section {
      height: auto;
      width: 100%;
      padding: 1rem;
  }

  .mini-me-banner {
    margin-top: 2rem;
    width: 9rem;
  }

  

    .heading-text-banner {
    background-color: #F6F4F2;
    width: 100%;
    justify-content: flex-start;
    box-shadow: none;
  }
 
 }

  @media (min-width: 120rem) { 
    .container {
      width: 1400px;
    }
 }
</style>
