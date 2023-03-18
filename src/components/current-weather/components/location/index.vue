<template>
  <div class="location fit-content">
    <div class="location__wrapper flex items-center">
      <MapPinIcon
        class="location__pin"
      />

      <address class="location__label cursor-pointer">
        Rio do Sul, SC
      </address>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

import MapPinIcon from '@/components/icons/map-pin/index.vue'

export default defineComponent({
  name: 'WeatherLocation',

  components: {
    MapPinIcon
  }
})
</script>

<style lang="scss" scoped>
  .location {
    &__pin,
    &__label {
      color: var(--purple2);
    }

    &__label {
      margin-inline: 8px 0;
      font: 700 1.4rem "Lato", sans-serif;
    }
  }
</style>
