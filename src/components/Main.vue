<template>
  <main>
    <section id="welcome">
      <div class="wrapper">
        <div class="welcome_top">
          <h2>Welcome to Avada Health</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius distinctio iste officiis dolorem minus itaque accusamus veritatis assumenda! Consectetur impedit consequatur provident. Accusamus accusantium excepturi veritatis eos neque eaque asperiores.</p>
        </div>
        <div class="welcome_bottom">
          <!-- CICLO FOR PER GENERARE LE INFO DI BENVENUTO -->
          <div v-for="(welcome_item, index) in welcome_bottom" :key="index" class="welcome_info">
            <img :src="require(`../${welcome_item.img}`)" alt="immagine">
            <h3>{{welcome_item.title}}</h3>
            <p>{{welcome_item.text}}</p>
          </div>

        </div>
      </div>
    </section>
    <section id="doctors">
      <div class="wrapper">
        <div class="doctors_top">
          <img src="../assets/img/icon-5.png" alt="icon">
          <h2>Meet Our Doctors</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?</p>
        </div>
        <div class="doctors_bottom">
          <!-- CICLO FOR PER GENERARE LE CARD DEI DOTTORI -->
          <div v-for="(doctor, index) in doctors" :key="index" class="doctor_card">
            <img :src="require(`../${doctor.img}`)" alt="immagine">
            <h4>{{doctor.name}}</h4>
            <h5>{{doctor.profession}}</h5>
            <p>{{doctor.biography}}</p>
            <div>
              <i :class="doctor.facebook" class="facebook"></i>
              <i :class="doctor.twitter" class="twitter"></i>
              <i :class="doctor.instagram" class="instagram"></i>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="services">
      <div class="wrapper">
        <div class="services_top">
          <img src="../assets/img/icon-6.png" alt="icon">
          <h2>Our Health Services</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?</p>
        </div>
        <div class="services_bottom">
          <!-- CICLO V-FOR PER GENERARE LE CARTE DEI SERVIZI -->
          <div v-for="(service, index) in services" :key="index" class="service">
            <img :src="require(`../${service.img}`)" alt="immagine">
            <h3>{{service.title}}</h3>
            <p>{{service.text}}</p>
          </div>
        </div>
      </div>
    </section>
    <section id="facilities">

    </section>
  </main>
</template>

<script>
export default {
    name: 'Main',
    data() {
      return {
        welcome_bottom: [
          {
            title: 'Same Day Appointmnet',
            img: 'assets/img/icon-1.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius distinctio iste'
          },
          {
            title: 'World Class Facilities',
            img: 'assets/img/icon-2.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius distinctio iste'
          },
          {
            title: 'Expert Doctors',
            img: 'assets/img/icon-3.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius distinctio iste'
          },
          {
            title: 'Complementary Therapies',
            img: 'assets/img/icon-4.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius distinctio iste'
          },
        ],
        doctors: [
          {
            name: 'Jon Snow',
            profession: 'Anesthesiologist',
            biography: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?',
            facebook: 'fab fa-facebook-square',
            twitter: 'fab fa-twitter-square',
            instagram: 'fab fa-instagram-square',
            img: 'assets/img/doctor-1.jpg',
          },
           {
            name: 'Tony Stark',
            profession: 'Cardiologist',
            biography: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?',
            facebook: 'fab fa-facebook-square',
            twitter: 'fab fa-twitter-square',
            instagram: 'fab fa-instagram-square',
            img: 'assets/img/doctor-2.jpg',
          },
           {
            name: 'Anna Smith',
            profession: 'Nurse Practitioner',
            biography: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?',
            facebook: 'fab fa-facebook-square',
            twitter: 'fab fa-twitter-square',
            instagram: 'fab fa-instagram-square',
            img: 'assets/img/doctor-3.jpg',
          },
        ],
        services: [
          {
            title: 'Rehabilitation center',
            img: 'assets/img/icon-14.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?',
          },
          {
            title: 'Dental Implants',
            img: 'assets/img/icon-15.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?',
          },
          {
            title: 'Medicine Research',
            img: 'assets/img/icon-16.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?',
          },
          {
            title: 'Blood Bank',
            img: 'assets/img/icon-11.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?',
          },
          {
            title: 'Pharmaceutical advice',
            img: 'assets/img/icon-12.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?',
          },
          {
            title: 'Medical counceling',
            img: 'assets/img/icon-13.png',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum quibusdam consequuntur error itaque, nostrum explicabo harum sint? Molestiae praesentium voluptatibus fugiat perferendis cum sequi hic, unde deleniti modi iste aperiam?',
          },
        ],
      }
    }
}
</script>

<style lang="scss">
@import '../style/General.scss';

#welcome {
  width: 100%;
  margin-top: 50px;
}

.welcome_top {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  padding: 20px;

  h2 {
    font-size: 30px;
    font-weight: 300;
    color: $primary_title_color;
  }

  p {
    width: 50%;
    line-height: 40px;
    text-align: center;
    color: $secondary_text_color;
  }
}

.welcome_bottom {
  display: flex;
  
  .welcome_info {
    width: calc(100% / 4);
    text-align: center;
    padding: 20px;

    h3 {
      font-weight: 300;
      text-transform: uppercase;
      color: $primary_title_color;
      padding: 10px 0;
    }

    p {
      line-height: 40px;
      color: $secondary_text_color;
    }
  }
}

#doctors {
  width: 100%;
  background-color: #F7F7F7;
}

.doctors_top {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  text-align: center;
  padding: 40px;

  h2 {
    font-size: 50px;
    font-weight: 300;
    color: $primary_title_color;
    text-transform: uppercase;
    margin: 20px 0 30px;

    &::after {
      content: "";
      display: block;
      width: 65%;
      height: 1px;
      background-color: $secondary_text_color;
      margin: 15px 0 0 70px;
    }
  }

  p {
    width: 40%;
    color: $secondary_text_color;
    line-height: 35px;
  }
}

.doctors_bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.doctor_card {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  width: calc(100% / 3);
  padding: 30px;

  h4 {
    font-size: 30px;
    font-weight: 300;
    color: #081425;
    padding: 10px;
  }

  h5 {
    font-size: 25px;
    font-weight: 300;
    color: #081425;
    padding: 10px;
  }

  p {
    color: $secondary_text_color;
    line-height: 35px;
    padding: 10px;
  }
  
  i {
    margin-right: 5px;
    margin-top: 10px;
    font-size: 25px;
    padding: 10px;
  }
}

.services_top {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  text-align: center;
  padding: 40px;

  h2 {
    font-size: 50px;
    font-weight: 300;
    color: $primary_title_color;
    text-transform: uppercase;
    margin: 20px 0 30px;

    &::after {
      content: "";
      display: block;
      width: 65%;
      height: 1px;
      background-color: $secondary_text_color;
      margin: 15px 0 0 70px;
    }
  }

  p {
    width: 40%;
    color: $secondary_text_color;
    line-height: 35px;
  }
}

.services_bottom {
  display: flex;
  flex-wrap: wrap;

  .service {
    width: calc(100% / 3);
    text-align: center;
    padding: 20px;

    h3 {
      font-weight: 300;
      text-transform: uppercase;
      color: $primary_title_color;
      padding: 10px 0;
    }

    p {
      line-height: 40px;
      color: $secondary_text_color;
    }
  }
}
</style>