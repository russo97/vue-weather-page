<template>
  <section class="curweather">
    <div class="curweather__wrapper w-full h-full relative">
      <LazyPrimaryCloudIcon
        class="curweather__cloud curweather__cloud--primary absolute"
      />

      <LazySecondaryCloudIcon
        class="curweather__cloud curweather__cloud--secondary absolute"
      />
    </div>
  </section>
</template>

<script>
import { defineComponent, defineAsyncComponent } from 'vue'

const LazyPrimaryCloudIcon = defineAsyncComponent(() => import(
  /* webpackChunkName: "lazy-primary-cloud-icon" */ '@/components/icons/primary-cloud/index.vue'
))

const LazySecondaryCloudIcon = defineAsyncComponent(() => import(
  /* webpackChunkName: "lazy-secondary-cloud-icon" */ '@/components/icons/secondary-cloud/index.vue'
))

export default defineComponent({
  name: 'CurrentWeather',

  components: {
    LazyPrimaryCloudIcon,
    LazySecondaryCloudIcon
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
      background: var(--purple1) url('@/assets/images/weather-bg.webp') center / cover no-repeat;
    }

    &__cloud {
      &--primary {
        z-index: 2;
        fill: var(--white);
        width: 27.4%;
        top: 0;
        left: 0;
        transform: translate(-36.496%, -8.363%);
      }

      &--secondary {
        z-index: 1;
        fill: var(--gray1);
        width: 22.725%;
        top: 0;
        left: 0;
        transform: translate(2.750%, -22.984%);
      }
    }
  }
</style>
