<template>
  <div class="app w-full h-full">
    <div class="app__wrapper"></div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App'
})
</script>

<style lang="scss" scoped>
  .app {
    background: transparent url("./assets/images/background.webp") center / cover no-repeat;
  }
</style>
