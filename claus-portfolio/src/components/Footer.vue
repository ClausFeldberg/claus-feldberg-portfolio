<template>
  <div id="footer" class="container"> 
      <div class="socials-wrapper">
          <div class="socials-container">
            <i class="fab fa-facebook-square"></i>
            <i class="fab fa-twitter"></i>
            <i class="fab fa-instagram"></i>
            <i class="fab fa-youtube"></i>
          </div>
          <div class="contact-banner">
            <div class="contact-item">
                <i class="fas contact-ico fa-phone"></i>
                <span class="contact-value">+45 30 25 44 61</span>
            </div>
            <div class="contact-item">
                <i class="fas contact-ico fa-envelope-open"></i>
                <span class="contact-value">claus@gmail.com</span>
            </div>
            <div class="contact-item">
                <i class="fab contact-ico fa-linkedin-in"></i>
                <span class="contact-value">Claus Feldberg</span>
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

<style scoped >
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

    .contact-item {
        margin-right: 1.5rem;
        transition: 0.2s ease;
        cursor: pointer;
    }

     .contact-item:hover {
        opacity: 0.7;
    }

    .fab {
         color: whitesmoke;
        opacity: 0.8;
        font-size: 2.2rem;
        cursor: pointer;
    }

    .contact-banner {
        display: flex;
        width: auto;
        padding: 1rem;
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

    .contact-ico{
        color: aliceblue;
        margin-right: 0.5rem;
        font-size: 1.5rem;
    }

    .contact-value{
        padding: 0;
        margin: 0;
        font-size: 1rem;
        font-family: 'Antonio', sans-serif;
        color: whitesmoke;
        opacity: 0.6;
        font-family: 'Bebas Neue', cursive;
    }

          @media (max-width: 600px) { 
              .contact-banner {
                  display: none;
              }
          }
</style>
