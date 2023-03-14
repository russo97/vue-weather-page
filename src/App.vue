<template>
  <main class="app w-full h-full">
    <div class="app__wrapper h-full">
      <Suspense>
        <LazyCurrentWeather />

        <template #fallback>
          loading
        </template>
      </Suspense>
    </div>
  </main>
</template>

<script>
import { defineComponent, defineAsyncComponent } from 'vue'

const LazyCurrentWeather = defineAsyncComponent({
  loader: () => import(
    /* webpackChunkName: "lazy-current-weather" */ './components/current-weather/index.vue'
  )
})

export default defineComponent({
  name: 'App',

  components: {
    LazyCurrentWeather
  }
})
</script>

<style lang="scss" scoped>
  .app {
    background: transparent url("./assets/images/background.webp") center / cover no-repeat;
  }
</style>
