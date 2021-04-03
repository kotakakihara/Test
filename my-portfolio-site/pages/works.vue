<template>
  <div class="works">
    <v-container class="works__header"></v-container>

  <v-container class="works__main">
    <v-row>
      <v-col class="works__title">
        <h1>Works</h1>
      </v-col>
    </v-row>

    <div class="works__items">
      <div class="works__item" v-for="item in items" :key="item.title">
        <div>{{ item.explain }}</div>
        <a :href="item.url" target="_blank" rel="noopener noreferrer"><img :src="item.image" alt=""></a>
      </div>
    </div>
  </v-container>
</div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: '自作Todoリスト１', explain: 'My To Do!', url: 'https://kotakakihara.github.io/kktodo.github.io/', image: require('../assets/images/myTodos1.png') },
        { title: '自作Todoリスト2', explain: 'My To Do!2', url: 'https://kotakakihara.github.io/portfolio-kktodo2/', image: require('../assets/images/myTodos2.png') },
        { title: 'F-FlameWork', explain: 'Nuxt', url: '', image: '' },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.works {
  font-weight: bold;
  &__title {
    border-bottom: 1px solid black;
  }
  &__item {
    display: inline-block;
    color: black;
    height: 200px;
    width: 200px;
    box-sizing: border-box;
    border-radius: 44px;
    background: linear-gradient(145deg, #ffffff, #e6e6e6);
    box-shadow:  27px 27px 54px #b5b5b5, -27px -27px 54px #ffffff;
    margin: 32px;
    overflow:hidden;
    div {
      text-align: center;
    }
    a,
    a > img {
      object-fit: cover;
      height: 100%;
      width: 100%;
    }
  }
}
</style>
