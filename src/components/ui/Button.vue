<template>
  <button :class="['btn', `btn_${color}`]">{{ label }}</button>
</template>

<script setup>
const props = defineProps({
  label: {
    type: String,
    default: 'Button'
  },
  color: {
    type: String,
    default: 'primary'
  }
})
</script>
<style lang="scss">
.btn {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px 16px;
  border-radius: 8px;
  border: none;

  font-weight: 700;
  font-size: 16px;
  line-height: 20px;
  transition: .3s ease-in-out;
  &_primary {
    background: var(--primary);
    color: var(--txt-black-1);
    &:hover {
      background: var(--primary-hover);
    }
  }
  &_secondary {
    background: var(--black-light);
    color: var(--white);
    &:hover {
      background: var(--black-primary);
      color: var(--white);
    }
  }
  &_outline {
    background: transparent;
    border: 1px solid var(--outline);
    &:hover {
      background: var(--txt-black-1);
      border: 1px solid var(--txt-black-1);
      color: var(--white);
    }
  }
}
</style>
