<template>
  <div class="curtemperature">
    <div class="curtemperature__wrapper">
      <h1 class="curtemperature__temperature relative">
        18
      </h1>

      <div class="curtemperature__minmax flex justify-center mt-1">
        <strong class="curtemperature__temp curtemperature__temp--max">
          22º
        </strong>

        <strong class="curtemperature__temp curtemperature__temp--min">
          16º
        </strong>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CurrentTemperature'
})
</script>

<style lang="scss" scoped>
  .curtemperature {
    margin: 60px 0 0;
    align-self: center;

    &__temperature {
      color: var(--white);
      font: 700 clamp(4rem, -13.1429rem + 45.7143vw, 8.8rem) / 10.6rem "Lato", sans-serif;

      &::after {
        content: "º C";
        position: absolute;
        top: 12px;
        left: 100%;

        line-height: 1;
        font-size: 2.4rem;
        white-space: nowrap;
        color: var(--purple3);
      }
    }
  }
</style>
