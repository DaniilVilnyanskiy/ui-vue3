<template>
  <div class="">
    <h3 class="mb-5">Ui Inputs</h3>
    <Input type="search" placeholder="Иван" title="Имя"/>
    <Input type="search" placeholder="Иванов" title="Фамилия"/>
  </div>
</template>

<script>
import Input from '../../components/ui/Input.vue'
export default {
  components: {
    Input,
  }
}
</script>

<style lang="scss">

</style>
