<template>
  <main>
    <section id="welcome">
      <div class="wrapper">
        <div class="welcome_top">
          <h2>Welcome to Avada Health</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius distinctio iste officiis dolorem minus itaque accusamus veritatis assumenda! Consectetur impedit consequatur provident. Accusamus accusantium excepturi veritatis eos neque eaque asperiores.</p>
        </div>
        <div class="welcome_bottom">
          <div v-for="(welcome_item, index) in welcome_bottom" :key="index" class="welcome_info">
            <img :src="require(`../${welcome_item.img}`)" alt="immagine">
            <h3>{{welcome_item.title}}</h3>
            <p>{{welcome_item.text}}</p>
          </div>

        </div>
      </div>
    </section>
    <section id="doctors">

    </section>
    <section id="services">

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
        ]
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
    color: $secondary_text_color;
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
      color: $secondary_text_color;
      padding: 10px 0;
    }

    p {
      line-height: 40px;
      color: $secondary_text_color;
    }
  }
}
</style>