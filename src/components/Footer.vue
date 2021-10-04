<template>
  <footer>
      <section class="footer_top">
        <div class="footer_brand_info">
          <div class="footer_logo">
            <img src="../assets/img/medical_logo_1x_dark.png" alt="Logo">
          </div>
          <div class="footer_brand_description">
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aperiam inventore eveniet placeat at quidem sit quas excepturi ipsum magni quaerat. Officia itaque quibusdam magni ducimus totam quos, cumque soluta sunt? Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolore deleniti dignissimos fugit hic, neque amet eveniet incidunt nostrum totam odio minus nam, voluptate ut cumque iusto omnis vel officia dolorem.</p>
          </div>
          <div class="brand_social_accounts">
            <h4>Learn More About US</h4>
            <i class="fab fa-facebook-square facebook"></i>
            <i class="fab fa-twitter-square twitter"></i>
            <i class="fab fa-youtube-square youtube"></i>
            <i class="fab fa-instagram-square instagram"></i>
          </div>
        </div>

        <div class="footer_brand_contacts">
          <h4>Contact Information</h4>
          <div>
            <i class="fas fa-map-marker-alt"></i>
            <span>121 King Street, London United Kingdom</span>
          </div>
          <div>
            <i class="fas fa-phone"></i>
            <span>1.800.458.556</span>
          </div>
        </div>

        <div class="medical_departments">
          <h4>Medical Departments</h4>
          <ul>
            <li v-for="(link, index) in footer_nav" :key="index"><i :class="link.arrow"></i><a href="#">{{link.text}}</a></li>
          </ul>
          <button>Wiew Our Departments</button>
        </div>
      </section>

      <section class="footer_bottom">
        <div class="copyright">
          <p>© Copiryght 2012-2020</p>
          <p>Avada Theme by <strong>Theme Fusion</strong></p>
          <p>All Rights Reserved</p>
          <p>Powered by <strong>Wordpress</strong></p>
        </div>

        <div class="footer_help">
          <div class="support">
            
          </div>
        </div>
      </section>
  </footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
      return {
        footer_nav: [
          {
            text: 'Cardiology',
            arrow: 'fas fa-chevron-circle-right',
          },
          {
            text: 'Pediatrics',
            arrow: 'fas fa-chevron-circle-right',
          },
          {
            text: 'Diabetes Care',
            arrow: 'fas fa-chevron-circle-right',
          },
          {
            text: 'Pre-natel Care',
            arrow: 'fas fa-chevron-circle-right',
          },
          {
            text: 'Ultrasound Echocardiogram',
            arrow: 'fas fa-chevron-circle-right',
          },
        ]
      }
    }
}
</script>

<style lang="scss">
@import '../style/General.scss';

footer {
  width: 100%;
  height: 500px;
  padding: 50px;

  .footer_top {
    display: flex;
    justify-content: flex-start;
    align-items: flex-start;
    height: 90%;
    color: $secondary_text_color;

    .footer_brand_info {
      width: calc(100% / 3);
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
      padding: 20px;

      .footer_logo {
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        margin-bottom: 10px;
      }

      p {
        width: 100%;
        margin-bottom: 15px;
      }

      .brand_social_accounts {
        width: 100%;
        border-top : 1px solid $secondary_text_color;
        margin-top: 10px;

        h4 {
          text-transform: uppercase;
          margin-top: 5px;
        }

        i {
          margin-right: 5px;
          margin-top: 10px;
          font-size: 25px;
        }
      }
    }

    .footer_brand_contacts {
      width: calc(100% / 3);
      padding: 20px;

      h4 {
        margin-bottom: 50px;
        text-transform: uppercase;

        &::after {
          content: '';
          display: block;
          width: 30px;
          height: 2px;
          background-color: $brand_color;
          margin-top: 20px
        }
      }

      i {
        color: $brand_color;
        margin-right: 15px;
      }
    }

    .medical_departments {
      width: calc(100% / 3);
      padding: 20px;

      h4 {
        margin-bottom: 50px;
        text-transform: uppercase;

        &::after {
          content: '';
          display: block;
          width: 30px;
          height: 2px;
          background-color: $brand_color;
          margin-top: 20px
        }
      }

      ul {
        list-style: none;

        li {
          i {
            color: $brand_color;
          }

          a { 
            margin-left: 10px;
            text-decoration: none;
            color: $secondary_text_color;
          }
        }

        
      }

      button {
        margin-top: 50px;
        background-color: white;
        padding: 10px 30px;
        border: 1px soldi black;
        cursor: pointer;
      }
    }
  }

  .footer_bottom {
    width: 100%;
    height: 10%;
    background-color: #f1efef;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .copyright {
      display: flex;
      justify-content: flex-start;
      align-items: center;
      height: 100%;
      color: $secondary_text_color;
      margin-left: 15px;

      p {
        margin: 0 5px;
        padding: 0 5px;
        
        &:after {
          content: '';
          width: 1px;
          height: 12px;
          display: inline-block;
          margin-left: 5px;
          background-color: $secondary_text_color;
        }
      }
    }
  }
}
</style>