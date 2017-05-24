<template>
  <div>
  	<transition-group name="fade">
  		<podcast-simple :key="1"></podcast-simple>
	  	<podcast-simple :key="2"></podcast-simple>
	  	<podcast-simple :key="3"></podcast-simple>
	  	<podcast-simple :key="4"></podcast-simple>
  	</transition-group>
  	<a href="#" class="load-more">Load older podcasts</a>
  </div>
</template>

<script>
import PodcastSimple from './podcasts/Simple'

export default {
  name: 'home',
  components: {
  	PodcastSimple
  }
}
</script>

<style lang="scss">
	.load-more {
		display: block;
		width: 100%;
		padding: 20px;
		text-decoration: none;
		background-color: #fff;
		text-align: center;
		color: inherit;
		margin-bottom: 40px;
		font-weight: 500;
	}
	.fade-enter-active, .fade-enter-leave {
		transition: opacity 500ms ease-in-out;
	}
	.fade-enter, .fade-leave-to {
		opacity: 0;
	}
</style>