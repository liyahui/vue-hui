<template>
  <button
    class="hui-btn"
    :class="classNames">
    <span><slot></slot></span>
  </button>
</template>

<script>
  export default {
    props: {
      type: {
        type: String,
        default: ''
      }
    },

    computed: {
      classNames () {
        return {
          [`hui-btn-${this.type}`]: this.type
        }
      }
    }
  }
</script>

<style lang="scss">
  .hui-btn {
    display: inline-block;
    cursor: pointer;
    outline: none;
    border: 1px solid #d9d9d9;
    border-radius: 4px;
    background-color: #fff;
    color: rgba(0,0,0,.65);
    padding: 4px 15px;
    font-size: 12px;
    font-weight: bold;
    line-height: 1.5; 
  }

  .hui-btn:hover {
    color: #108ee9;
    border-color: #108ee9;
  }

  .hui-btn-primary {
    border-color: #108ee9;
    background-color: #108ee9;
    color: #fff;
  }

  .hui-btn-primary:hover {
    color: #fff;
    background-color: #49a9ee;
    border-color: #49a9ee
  }

  .hui-btn-danger {
    color: #fff;
    background-color: #f04134;
    border-color: #f04134
  }

  .hui-btn-danger:hover {
    color: #fff;
    background-color: #f46e65;
    border-color: #f46e65;
  }
</style>
