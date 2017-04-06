<template>
  <div id="app">
    <Button type="primary">Primary</Button>
    <Button>Default</Button>
    <Button type="danger">Danger</Button>
  </div>
</template>

<script>
import Button from './components/button'

export default {
  name: 'app',
  components: {
    Button
  }
}
</script>

<style>
  @import '~normalize.css';

  * {
    box-sizing: border-box;
  }

  body {

  }
</style>
