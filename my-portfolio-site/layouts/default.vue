<template>
  <v-app light>
    <v-app-bar
      :absolute="!bar"
      color="white"
      elevate-on-scroll
      scroll-target="#scrolling-techniques-7"
      app
    >
      <v-row>
        <v-col>
          <v-tabs centered v-model="tab">
            <v-tab v-for="item in items" :key="item.title" :to="item.url">
              {{ item.title }}
            </v-tab>
          </v-tabs>
        </v-col>
      </v-row>
    </v-app-bar>

    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<style scoped>
.v-tab:hover {
  opacity: 0.7;
}
.v-tab--active {
  background-color: black;
}
v-tabs-slider-wrapper {
  box-shadow: 1px;
}
</style>
<script>
export default {
  data() {
    return {
      bar: true,
      fixed: true,
      tab: null,
      items: [
        { title: 'TOP', url: '/' },
        { title: 'WORKS', url: '/works' },
        { title: 'CONTACT', url: '/contact' },
      ],
      title: 'Kackey!.Inc',
    }
  },
}
</script>
