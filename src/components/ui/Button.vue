<template>
  <button
      :class="['btn', `btn_${color}`]"
      @click="handlerClick"
  >
    <span>{{ label }}</span>
    <Icon name="add" />
  </button>
</template>

<script>
import Icon from "./Icon.vue";
export default {
  components: {
    Icon
  },
  props: {
    label: {
      type: String,
      default: 'Button'
    },
    color: {
      type: String,
      default: 'primary'
    }
  },
  data () {
    return {
      test: 'test'
    }
  },
  methods: {
    handlerClick(e) {
      this.$emit("clickButton", this);
    }
  }
}
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
  svg {
    margin-left: 10px;
    transition: .3s ease-in-out;
  }
  &_primary {
    background: var(--primary);
    color: var( --black-primary);
    svg {
      fill: var(--black-primary);
    }
    &:hover {
      background: var(--primary-hover);
    }
  }
  &_secondary {
    background: var(--black-light);
    color: var(--white);
    svg {
      fill: var(--white);
    }
    &:hover {
      background: var(--black-primary);
      color: var(--white);
    }
  }
  &_outline {
    background: transparent;
    border: 1px solid var(--outline);
    svg {
      fill: var(--black-primary);
    }
    &:hover {
      background: var( --black-primary);
      border: 1px solid var( --black-primary);
      color: var(--white);
      svg {
        fill: var(--white);
      }
    }
  }
}
</style>
