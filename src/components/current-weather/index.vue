<template>
  <section class="curweather">
    <div class="curweather__wrapper w-full h-full"></div>
  </section>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CurrentWeather',

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
      background-color: purple;
    }
  }
</style>
