<template>
    <div class="podcast">
    	<a href="#" class="podcast__play">
    		<img src="../../assets/img/player.svg" alt="" class="podcast__playbutton">
    	</a>
    	<div class="podcast__details">
	    	<div class="podcast__sub">2 days ago</div>
	    	<h1 class="podcast__header">
	    		<a href="#">Lorem ipsum dolor sit.</a>
	    	</h1>
	    	<p>
	    		Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil et quis veritatis similique eum aliquid mollitia perferendis iusto reprehenderit sed?
	    	</p>
	    </div>
    </div>
</template>

<script>
export default {
	name: 'podcast-simple'
}
</script>

<style lang="scss">
	@import '~styles/variable';

	.podcast {
		background-color: #fff;
		display: flex;
		min-height: 240px;
		border-radius: $global-radius;
		margin-bottom: 40px;
		box-shadow: 0 5px 10px rgba(#000000, .05);
		overflow: hidden;
		
		&__details {
			flex: 1;
			padding: 40px;
		}
		&__sub {
			font-weight: 500;
		}
		&__header {
			font-size: 1.6em;
			a {
				text-decoration: none;
			}
		}	
		&__play {
			width: 15%;
			background-color: $blue;
			align-items: center;
			justify-content: center;
			border-top-left-radius: $global-radius;
			border-bottom-left-radius: $global-radius;
			transition: margin-left 180ms ease-in-out;
			overflow: hidden;

			&:hover {
				.podcast__playbutton {
					transform: scale(3.3) rotate(-10deg);
					opacity: 1;
				}
			}
			&--hidden {
				margin-left: -15%;
			}
		}

		&__playbutton {
			color: #222;
			opacity: .4;
			width: 60%;
			transition: all 200ms ease-in-out;
		}
	}

	@media only screen and (min-width: 768px){
		.podcast__play {
			display: flex;
		}
	}
</style>