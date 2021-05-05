<template>
  <div class="container">
      <div class="header-wrapper">
          <div class="mini-me-wrapper">
            <img class="mini-me-banner" src="../assets/graphics/mini me.png" alt="">
          </div>
          <div class="heading-text-banner">
            <div class="text-wrapper">
              <h1 class="header-heading">Claus Feldberg</h1>
              <h1 class="header-heading">Portfolio.</h1>
            </div>
          </div>
      </div>
      <v-parallax height="750" src="../assets/pics/miig.jpg">
        <div class="parallax-wrapper">
          <div class="first-section-wrapper">
            <h2 class="section-heading">Lorem ipsum</h2>
            <p class="section-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil in culpa deleniti ipsam. Magnam earum officiis at quos veniam dicta porro nulla amet quibusdam? Aliquid facere cum cupiditate earum neque.</p>
        </div>
        </div>
      </v-parallax>
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
                   <p class="section-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil in culpa deleniti ipsam. </p>
              </div>
          </div>
          <!-- <div class="triangular-shaper">

          </div> -->
      </div>
      <div class="video_wrapper">
          <iframe  id="myVideo" width="560" height="315" src="https://www.youtube.com/embed/tZ7OPH0PZfE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      <div class="third-section">
         <div class="left-side-wrapper">
             <h2 class="section-heading">Lorem ipsum</h2>
             <p class="section-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil in culpa deleniti ipsam. Magnam earum officiis at quos veniam dicta porro nulla amet quibusdam? Aliquid facere cum cupiditate earum neque.</p>
         </div>
         <div class="right-side-wrapper">

         </div>
      </div>
  </div>
</template>

<script>


  export default {
    name: 'Home',

    components: {
     
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
    padding: 2rem;
    height: auto;
    justify-content: flex-start;
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
    text-align: center;
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
        height:100vh;
        background-color: #e80002;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    #myVideo{
        width:55%;
        height:100%;
    }


</style>
