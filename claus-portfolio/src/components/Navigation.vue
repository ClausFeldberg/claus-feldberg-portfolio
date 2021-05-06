<template>
    <div class="container">
        <v-app-bar
                color="transparent"
                inverted-scroll="true"
                height="70"
                fixed="true"
                flat="true"
                class="app-bar-wrapper"
        >
            <div class="app-bar-control">
                <i class="fas fa-bars hamburger" @click="drawer = true"></i>
            </div>
        </v-app-bar>
        <v-navigation-drawer
                mobile-break-point="480"
                v-model="drawer"
                app="true"
                temporary
                color="transparent"
                height="100%"
                width="450"
        >

        <div class="nav-drawer">
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
                <a class="social-ico" href=""><i class="fab fa-spotify" ></i></a>
                <a class="social-ico" href=""><i class="fab fa-youtube"></i></a>
                <a class="social-ico" href=""><i class="fab fa-linkedin"></i></a>
                <a class="social-ico" href=""><i class="fab fa-instagram"></i></a>
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
                    { name: "ABOUT", path: "/#about-me" },
                    { name: "WORKS", path: "/#my-works" },
                    { name: "CONTACT", path: "/#footer" },
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
        background-image: url("../assets/graphics/spray.jpeg");
        background-size: cover;
        display: flex;
        flex-direction: column;
        align-items:center;

    }

    .nav-container{
        width:100%;
        height:100%;
        flex-direction: column;
        align-items: center;
        display: flex;
        justify-content:center;
    }

    .hit_box{
        width:100%;
        height: 100px;
        background:rgba(0,0,0,0.4);
        display: flex;
        margin-bottom: 0.5rem;
        border-radius: 10px;
        justify-content: center;
        align-items: center;
        background-color:black;
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
        font-family: 'Antonio', sans-serif;
        font-family: 'Bebas Neue', cursive;
        font-weight: 700;
        color: #ffffff !important;
    }

    .social-links{
        width:80%;
        height:20%;
        display: flex;
        justify-content:space-between;
        align-items:center;
        text-decoration: none;
    }

    .social-ico {
        color:  #F6F4F2;
        font-size: 2rem;
        display: flex;
        justify-content: center;
        align-items: center;
        transition: all 0.2s;
        width: 3.5rem;
        height: 3.5rem;
        padding: 0;
        margin: 0;
        border-radius:10px;
        background-color: black;
    }

    .social-ico:hover{
        transform: scale(1.1);
        background-color: #F6F4F2;
        color: black;
    }

    .social-ico:hover > .fab{
        transform: scale(1.1);
        background-color: #F6F4F2;
        color: black;
    }


    @media (max-width: 600px) {

        .fab{
            font-size:30px;
        }

        a{
            font-size: 25px;
        }

        .nav-drawer{
            justify-content:center;
            width:100%;
            height:100%;
        }

        .hit_box{
            width:100%;
            margin: 0;
            padding: 0;
            height: 60px;
        }
    }



</style>
