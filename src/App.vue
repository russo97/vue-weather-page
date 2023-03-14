<template>
  <main class="app w-full h-full">
    <div class="app__wrapper h-full">
      <HomeView />
    </div>
  </main>
</template>

<script>
import { defineComponent } from 'vue'

import HomeView from './views/home/index.vue'

export default defineComponent({
  name: 'App',

  components: {
    HomeView
  }
})
</script>

<style lang="scss" scoped>
  .app {
    background: transparent url("./assets/images/background.webp") center / cover no-repeat;

    &__wrapper {
      padding: 32px 32px 0;
    }
  }
</style>
