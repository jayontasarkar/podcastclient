<template>
  <div id="app">
    <top-header></top-header>
    <div class="container">
      <home></home>
    </div>
  </div>
</template>

<script>
import TopHeader from './components/TopHeader'
import Home from './components/Home'

export default {
  name: 'app',
  components: {
    TopHeader,
    Home
  }
}
</script>

<style lang="scss">
  @import '~styles/variable';

  * {
    box-sizing: border-box;
  }
  body {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    background-color: #edeff0;
    margin-top: calc(#{$header-height} + calc(#{$header-padding} * 2));
  }
  p {
    line-height: 1.5;
  }
  a {
    color: rgba($blue, .80);
    transition: color 100ms ease-in;

    &:hover {
      color: $blue;
    }
  }
  .container {
    max-width: 780px;
    margin: 0 auto;
    flex: 1;
  }
</style>
