<template>
    <div class="container">
        <v-app-bar
                color="transparent"
                inverted-scroll="true"
                height="70"
                fixed="true"
                flat="false"
                class="app-bar-wrapper"
                elevate-on-scroll= "true"
        >
            <div class="app-bar-control">
                <i class="fas fa-bars hamburger" @click="drawer = true"></i>
                <!-- <img class="logo_wrapper "  src="../assets/icons/Json-logo.svg"  alt=""> -->
            </div>
        </v-app-bar>

        <v-navigation-drawer
                mobile-break-point="480"
                v-model="drawer"
                app="true"
                temporary
                color="#0049FF"
                height="800"
                width="400"
        >

        <div class="nav-drawer">

            <!-- <div class="logo_banner">
                <img class="logo_wrapper2"  src="../assets/icons/Json-logo2.svg"  alt="">
            </div> -->

            <div class="nav-container">
                <li
                        class="shuffle"
                        v-for="(link, index) in navLinks"
                        v-bind:key="index"
                >
            <div class="hit_box">

                <a :href="link.path">

                  <span class="top">
                    <span>{{ link.name }}</span>
                  </span>
                  <span class="bottom">
                    <span>{{ link.name }}</span>
                  </span>
                </a>



            </div>
                </li>

            </div>

            <div class="social-links">
                <a href="https://open.spotify.com/artist/7jGExbES4WgzpAEABOzExn?si=O_MUUByGTaistRqFBMYFZw&fbclid=IwAR20TkqHF8cjNZKZUVC8WCDMoZct6_R7PdFEwpzT32XrxGpu7-UPQJO-_7w"><i class="fab fa-spotify" ></i></a>
                <a href="https://www.youtube.com/channel/UCPE5eGtUK832qKP5IJ9smGg"><i class="fab fa-youtube"></i></a>
                <a href=""><i class="fab fa-linkedin"></i></a>
                <a href="https://www.instagram.com/jasonraider/"><i class="fab fa-instagram"></i></a>
            </div>

        </div>


        </v-navigation-drawer>
    </div>
</template>

<script>

    export default {
        name: 'Navigation',

        data () {
            return {
                drawer: false,
                navLinks: [
                    { name: "HOME", path: "/" },
                    { name: "ABOUT", path: "/#about" },
                    { name: "WORKS", path: "/#my-works" },
                    { name: "CONTACT", path: "/#contact" },
                ],
            }
        },
    };
</script>

<style lang="scss" >

    .app-bar-control{
        display: flex;
        width:100%;
        height:auto;
        justify-content: space-between;
        align-items: center;
    }

    .logo_wrapper{
        margin-top:17px;
        width: 90px;
        height: 90px;
    }

    .hamburger{
        color:#F6F4F2;
        font-size: 2rem;
        background-color:#141824;
         background:rgba(0,0,0,0.6);
        width: 3.5rem;
        height: 3.5rem;
        border-radius: 15px;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        padding: 0;
    }


    a{
        position: relative;
        font-size: 40px;
        line-height: 40px;
        text-transform: uppercase;
        text-decoration: none;
        color: black;
        font-family: Poppins;
        font-weight:700;
        margin-top:70px;
        width:400px;
        height: 110px;
        overflow: hidden;
    }

    a > span{
        position: relative;
        display: block;
        height: 20px;
        overflow: hidden;
        transition: transform 0.3s;
        transition-delay: 0.1s;
    }


    a > span > span{
        top: 0;
        left: 0;
        position: absolute;
        text-align: center;
        width: 100%;
    }

    a > span.bottom > span{
        top: auto;
        bottom: 0;
        text-align: center;
    }


    a::after{
        content: "";
        display: block;
        position: absolute;
        top: 50%;
        left: 50%;
        width: 100%;
        height: 1px;
        background-color: black;
        transform: translate3d(-150%, -50%,0);
        transition: transform 0.3s;
    }


    .nav-drawer{
        width:100%;
        height:100%;
        display: flex;
        flex-direction: column;
        align-items:center;

    }

    .logo_banner{
        width: 100%;
        height:17%;
        display: flex;
        justify-content: center;
        align-items:flex-end;
    }



    .logo_wrapper2{
        width:120px;
        height: 120px;
    }

    .nav-container{
        width:100%;
        height:70%;
        flex-direction: column;
        align-items: center;
        display: flex;
        justify-content:center;
    }

    .hit_box{
        width:350px;
        height: 100px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color:black;
    }

    a:hover::after{
        transform: translate3d(-50%, -50%, 0);
    }

    a:hover .top{
        transform: translate3d(5%, 0, 0);
    }


    a:hover .bottom{
        transform: translate3d(-5%, 0, 0);
    }


    .hit_box:hover {
        -webkit-transform: scale(1.1);
        letter-spacing: 10px;
        -ms-transform: scale(1.1);
        transform: scale(1.1);
        transition: all 0.1s ease 0s;
    }

    li{
        list-style: none;
        margin-top:10px;
    }

    a{
        text-decoration: none;
        font-size: 50px;
        font-family: 'Poppins', sans-serif;
        font-weight: 700;
        color: #ffffff !important;
    }

    .social-links{
        width:85%;
        height:20%;
        display: flex;
        justify-content:space-around;
        align-items:flex-start;
    }

    .fab{
        color: black;
        font-size: 50px;
    }

    .fab:hover{
        -webkit-transform: scale(1.1);
        -ms-transform: scale(1.1);
        transform: scale(1.1);
        transition: all 0.5ms ease-out 10ms;
    }


    @media (max-width: 480px) {

        .logo_banner{
            height:5%;
            align-items: center;
        }

        .logo_wrapper2{
            width: 50px;
        }


        .fab{
            font-size:30px;
        }

        a{
            font-size: 25px;
        }

        .nav-drawer{
            justify-content:center;
            width:100%;
            height:70%;
        }

        .hit_box{
            width:300px;
            height: 60px;
        }
    }



</style>
