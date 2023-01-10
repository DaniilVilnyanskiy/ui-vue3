<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'

</script>

<template>
  <div class="body">
    <Header></Header>
    <router-view/>
  </div>
</template>

<style scoped lang="scss">
  @import "styles/global.scss";

</style>
