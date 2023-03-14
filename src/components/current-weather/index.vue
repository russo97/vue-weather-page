<template>
  <section class="curweather">
    <div class="curweather__wrapper w-full h-full">
      <LazyPrimaryCloudIcon
        class="curweather__cloud curweather--cloud--primary"
      />
    </div>
  </section>
</template>

<script>
import { defineComponent, defineAsyncComponent } from 'vue'

const LazyPrimaryCloudIcon = defineAsyncComponent(() => import(
  /* webpackChunkName: "lazy-primary-cloud-icon" */ '@/components/icons/primary-cloud/index.vue'
))

export default defineComponent({
  name: 'CurrentWeather',

  components: {
    LazyPrimaryCloudIcon
  },

  async setup () {
    return {}
  }
})
</script>

<style lang="scss" scoped>
  .curweather {
    aspect-ratio: 1;
    width: min(100%, 480px);

    &__wrapper {
      border-radius: 10px;
      background-blend-mode: luminosity;
      background: #8E87FA url('@/assets/images/weather-bg.webp') center / cover no-repeat;
    }

    &__cloud {
      fill: white;
      width: 27.29%;
    }
  }
</style>
