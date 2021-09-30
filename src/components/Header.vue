<template>
    <header>
      <!-- HEADER NAV -->
        <section id="header_nav">
            <div id="header_logo">
                <img src="../assets/img/medical_logo_1x_light.png" alt="Logo">
            </div>

            <nav class="primary_nav">
                <ul>
                    <li v-for="(link, index) in nav" :key="index"><a :class="(link.current) ? 'active' : null" href="#">{{link.text}}</a></li>
                    <li><button>Make an appointment</button></li>
                </ul>
            </nav>
        </section>
      <!-- HEADER CATCH PHRASE -->
        <section id="header_catch_phrase" class="wrapper">
            <h1>Caring<span>For Life</span></h1>
            <p>Kind words can be short and easy to speak, but their echoes are truly endless.Avada health focuses on you as if it was our own family</p>
            <button>Learn More</button>
        </section>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            nav: [ 
                {
                    text: 'Home',
                    current: true,
                },
                {
                    text: 'About',
                    current: false,
                },
                {
                    text: 'Department',
                    current: false,
                },
                {
                    text: 'Articles',
                    current: false,
                },
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../style/General.scss';

    header {
        width: 100%;
        height: 1110px;
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
                margin-right: 20px;

                ul {
                   display: flex;
                   justify-content: center;
                   align-items: center;
                   list-style: none;
                   
                   li {
                       margin: 0 20px;

                       a {
                           text-decoration: none;
                           color: $primary_text_color;
                           font-size: 20px;

                           &.active {
                                color: $brand_color;
                            }
                       }

                       button {
                           color: $primary_text_color;
                           text-transform: uppercase;
                           font-size: 15px;
                           padding: 10px;
                           border: none;
                           border-radius: 5px;
                           background-color: $brand_color;
                           cursor: pointer;
                       }
                   }
                }
            }

        }

        #header_catch_phrase {
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: flex-start;
                padding: 130px;

                h1 {
                    color: $primary_text_color;
                    font-size: 70px;
                    font-weight: 300;

                    span {
                        color: $brand_color;
                        margin-left: 10px;
                    }
                }

                p {
                    width: 460px;
                    font-size: 20px;
                    color: $primary_text_color;
                    margin: 20px 0;  
                }    
                
                button {
                    color: $primary_text_color;
                    text-transform: uppercase;
                    padding: 10px 30px;
                    font-size: 15px;
                    background-color: $brand_color;
                    border: none;
                    border-radius: 5px;
                    cursor: pointer;
                }
            }
    }
</style>