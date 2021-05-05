<template>
  <div class="container"> 
      <div class="socials-wrapper">
          <div class="socials-container">
            <i class="fab fa-facebook-square"></i>
            <i class="fab fa-twitter"></i>
            <i class="fab fa-instagram"></i>
            <i class="fab fa-youtube"></i>
          </div>
            <div class="contact-banner">
            <div class="contact-item">
                <i class="fas fa-phone"></i>
                <span>+45 897 452 721</span>
            </div>
                <div class="contact-item">
                <i class="fas fa-envelope-open"></i>
                <span>claus@gmail.com</span>
            </div>
        </div>
      </div>
      <div class="bottom-footer">
          <span class="paragraph">Created by Claus Feldberg |  {{ new Date().getFullYear() }} All rights reserved</span>
      </div>
  </div>
</template>

<script>
    export default {
        name: 'Footer',

         data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
    };
</script>

<style lang="scss" >
    .container {
        width: 100%;
        height: auto;
        display: flex;
        flex-direction: column;
    }
    .socials-wrapper {
        width: 100%;
        height: 7rem;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 4rem;
        background-color:#141824;
    }

    .bottom-footer {
        width: 100%;
        height: 3rem;
        background-color:#141824;
        display: flex;
        align-items: center;
        padding: 1rem;
        opacity: 0.9;
        justify-content: center;
        background:rgba(0,0,0,0.95);
    }

    .fab {
         color: whitesmoke;
        opacity: 0.8;
        font-size: 2.2rem;
        cursor: pointer;
    }

    .contact-banner {
        display: flex;
    }

    .socials-container {
        width: 15rem;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .paragraph {
        padding: 0;
        margin: 0;
        font-size: 0.9rem;
        font-family: 'Antonio', sans-serif;
        color: whitesmoke;
        opacity: 0.6;
        font-family: 'Bebas Neue', cursive;
    }
</style>
