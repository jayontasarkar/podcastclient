<template>
    <div class="player">
    	<div class="player__header">
    		<span>Now playing</span>: Podcast Title
    	</div>
    	<audio controls="controls" autoplay ref="player" class="player__audio"></audio>
    </div>
</template>

<script>
export default {
	name: 'player'
}
</script>

<style lang="scss">
	.player {
		width: 100%;

		&__audio {
			width: 100%;
		}
		&__header {
			font-weight: 500;
			margin-bottom: 20px;
		}
	}
</style>