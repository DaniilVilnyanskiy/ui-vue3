<template>
  <div class="body">
    <Header></Header>
    <div class="container">
      <Breadcrumbs />
    </div>
    <router-view/>
  </div>
</template>

<script lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Breadcrumbs from './components/ui/Breadcrumbs.vue';

export default {
  components: {
    Breadcrumbs,HelloWorld ,Header
  }
}
</script>
<style lang="scss">
  @import "styles/global.scss";

</style>
