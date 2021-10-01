<template>
  <footer>
      <section class="footer_top">
        <div class="footer_brand_info">
          <div class="footer_logo">
            <img src="../assets/img/medical_logo_1x_dark.png" alt="Logo">
          </div>
          <div class="footer_brand_description">
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aperiam inventore eveniet placeat at quidem sit quas excepturi ipsum magni quaerat. Officia itaque quibusdam magni ducimus totam quos, cumque soluta sunt?</p>
          </div>
          <div class="brand_social_accounts">
            <h5>Learn More About US</h5>
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

        <div class="medical_deparments">
          <h4>Medical Departments</h4>
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
    name: 'Footer'
}
</script>

<style lang="scss">
@import '../style/General.scss';

footer {
  width: 100%;
  height: 500px;

  .footer_top {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    color: $secondary_text_color;

    .footer_brand_info {
      width: calc(100% / 3);
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;

      .footer_logo {
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
      }

      p {
        margin-left: 20px;
      }

      .brand_social_accounts {
        width: 100%;
        border-top : 1px solid $secondary_text_color;

        .facebook {
          color:#0F92F3;
        }

        .twitter {
          color: #119AFB;
        }

        .youtube {
          color: #cc201f;
        }

        .instagram {
          color: #1D56A2;
        }
      }
    }

    .footer_brand_contacts {
      width: calc(100% / 3);
    }

    .medical_departments {
      width: calc(100% / 3);
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
        border-right: 1px solid $secondary_text_color;
      }
    }
  }
}
</style>