<template>
  <div class="page page--home">
    <div class="page__wrapper">
      <Suspense>
        <LazyCurrentWeather />

        <template #fallback>
          loading
        </template>
      </Suspense>
    </div>
  </div>
</template>

<script>
import { defineComponent, defineAsyncComponent } from 'vue'

const LazyCurrentWeather = defineAsyncComponent({
  loader: () => import(
    /* webpackChunkName: "lazy-current-weather" */ '@/components/current-weather/index.vue'
    )
})

export default defineComponent({
  name: 'HomeView',

  components: {
    LazyCurrentWeather
  }
})
</script>

<style lang="scss" scoped>
</style>
