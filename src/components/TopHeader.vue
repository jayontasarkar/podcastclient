<template>
  <header class="topheader">
    <div class="container">
      <p class="welcome">
        Oh, hi. <strong>Choose something to play.</strong>
      </p>
      <player></player> 
    </div>
  </header>
</template>

<script>
import Player from './player/Player'

export default {
  name: 'top-header',
  components: {
    Player
  }
}
</script>

<style lang="scss">
  @import '~styles/variable';

  .welcome {
    font-size: 1.1em;
    text-align: center;
  }
  .topheader {
    display: flex;
    align-items: center;
    width: 100%;
    height: 140px;
    background-color: #fff;
    position: fixed;
    left: 0; top: 0;
    padding: $header-padding;
    z-index: 2;
  }
</style>