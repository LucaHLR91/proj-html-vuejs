<template>
    <header>
      <!-- HEADER NAV -->
        <section id="header_nav">
            <div id="header_logo">
                <img src="../assets/img/medical_logo_1x_light.png" alt="Logo">
            </div>

            <nav class="primary_nav">
                <ul>
                    <li v-for="link in nav" :key="link"><a href="#">{{link}}</a></li>
                    <li><button>Make an appointment</button></li>
                </ul>
            </nav>
        </section>
      <!-- HEADER CATCH PHRASE -->
        <section id="header_catch_phrase">

        </section>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            nav: [
                'Home',
                'About',
                'Department',
                'Articles'
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../style/General.scss';

    header {
        width: 100%;
        height: 1231px;
        background-image: url('../assets/img/header-image-homepage.jpg');
        background-size: cover;
        background-repeat: no-repeat;

        #header_nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;

            #header_logo {
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .primary_nav {
                display: flex;
                justify-content: center;
                align-items: center;

                ul {
                   display: flex;
                   justify-content: center;
                   align-items: center;
                   list-style: none;
                   
                   li {
                       margin: 0 10px;

                       a {
                           text-decoration: none;
                           color: white;
                       }
                   }
                }
            }
        }
    }
</style>