<template>
  <button class="hui-btn" :class="classNames" :disabled="disabled" @click="handleClick">
    <span>
      <slot></slot>
    </span>
  </button>
</template>

<script>
  export default {
    name: 'HuiButton',
    props: {
      type: {
        type: String,
        default: ''
      },
      size: {
        type: String,
        default: ''
      },
      disabled: {
        type: Boolean,
        default: false
      }
    },
    computed: {
      classNames () {
        return {
          [`hui-btn-${this.type}`]: this.type,
          [`hui-btn-${this.size}`]: this.size
        }
      }
    },
    methods: {
      handleClick () {
        this.$emit('click')
      }
    }
  }
</script>

