<template>
  <div class="top">
    <v-row class="top__header" justify="center" align="center">
      <h1 class="top__title">DUAL CHICKEN DUCHs</h1>
      <h3 class="top__subtitle">Front-end portpolio and comic articles.</h3>
    </v-row>

    <v-container class="profile">
      <v-row>
        <v-col><h1>Profile</h1></v-col>
      </v-row>
      <v-row class="profile__face">
        <div class="profile__img">
          <img src="../assets/images/preview.png" />
          <div class="profile__covered"></div>
        </div>
      </v-row>
      <v-row class="profile__sumary">
        <p>
          2020年より東京都のWeb企業にて、フロントエンドエンジニアとして働いています。
        </p>
        <p>「〇〇〇」がモットーです。</p>
        <p><b>名称：</b>Kackey!</p>
        <p><b>所在地：</b>川崎市</p>
        <p><b>お問い合わせ：</b>〇〇@gmail.com</p>
        <p><b>コンテンツ：</b>ポートフォリオ成果物、絵、写真他。。。</p>
      </v-row>
    </v-container>

    <v-container>
      <v-row>
        <v-col><h1>Skill</h1></v-col>
      </v-row>
      <v-row>
        <v-col v-for="item in items" :key="item.title" class="skill__card">
          <div style="padding: 15px">
            <h3>{{ item.title }}</h3>
            <div></div>
            <div>
              <p>HTML5/SCSS</p>
              <p>~1年</p>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>

    <v-container>
      <v-row>
        <v-col><h1>Works</h1></v-col>
      </v-row>
    </v-container>

    <nuxt-link to="/works" style="color: black; float: right"
      >>> Works</nuxt-link
    >
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo,
  },

  data() {
    return {
      items: [
        { title: 'Design/Markup', lang: 'HTML5/SCSS', years: '~1年' },
        { title: 'FrontEnd', lang: 'ES6/Vue3', years: '~1年' },
        { title: 'F-FlameWork', lang: 'Nuxt', years: '~1年' },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.top {
  font-family: 'Century Gothic', 'Lato', sans-serif;
  &__header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    position: relative;
    text-align: center;
    padding: 0 2em;
  }
  &__title {
    font-size: 2rem;
    margin: 0;
    letter-spacing: 1rem;
  }
  &__subtitle {
    font-size: 1rem;
    letter-spacing: 0.3rem;
    opacity: 0.6;
  }
}
.profile {
  margin: 16px 0;
  &__img {
    display: block;
    margin:32px auto;
    height: 250px;
    width: 250px;
    border-radius: 50%;
    background-position: center;
    background-size: cover;
    border-radius: 50%;
    background: linear-gradient(145deg, #ffffff, #e6e6e6);
    box-shadow: 20px 20px 60px #a8a8a8, -20px -20px 60px #ffffff;
    position: relative;
    img {
      height: 100%;
      width: 100%;
      border-radius: 50%;
    }
  }
  &__covered {
    height: inherit;
    width: inherit;
    border-radius: 50%;
    background: transparent;
    box-shadow: inset 14px 14px 28px #c4c4c4, inset -14px -14px 28px #ffffff;
    position: absolute;
    z-index: 100;
    top: 0px;
    left: 0px;
  }
  &__sumary {
    text-align: center;
    display: block;
    margin: 32px auto;
    p {
      // text-align: left;
    }
  }
}
.skill {
  &__card {
    border-radius: 50px;
    background: linear-gradient(145deg, #ffffff, #e6e6e6);
    box-shadow: 20px 20px 60px #a8a8a8, -20px -20px 60px #ffffff;
    margin: 16px;
  }
}
</style>