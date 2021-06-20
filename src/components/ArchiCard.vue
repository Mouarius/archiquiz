<template>
  <div class="archicard" @click="revealAnswer">
	  <div :class="{flipped: isRevealed}" class="archicard-inner">
		<div class="card verso">
			<h1>Une maison à Trentemoult</h1>
			<h2>Architecte inconnu, 1990</h2>
		</div>
		<div class="card recto">
			<img src="/src/assets/images/archi1.jpg" alt="" srcset="">	
		</div>

	  </div>
  </div>
</template>

<script>
export default {
	name:"ArchiCard",
	data(){
		return({
			isRevealed: false

		}
		)
	},
	methods:{
		revealAnswer(){
			this.isRevealed = !this.isRevealed
			console.log("clicked !")
			console.log(this.isRevealed)
		}
	}

}
</script>

<style lang="scss">
.archicard{
	width: 320px;
	height: 480px;
	cursor: pointer;
	perspective: 2000px;
		
}
.archicard-inner{
	transition: transform 0.6s ease;
}
.flipped{
	transform: rotateY(180deg);
}
.card{
	transform-style: preserve-3d;
	display: block;
	position:absolute;
	width: 320px;
	height: 480px;
	box-sizing: border-box;
	overflow: hidden;
	margin-top: 24px;
	border-radius: 24px;
	border: solid 1px rgba(0, 0, 0, 0.1);
	box-shadow: 0px 8px 20px rgba(0, 0, 0, 0.9);
	color: rgb(247, 247, 247);
	background-color: rgb(29, 29, 29);
}
.recto {
	-webkit-backface-visibility: hidden; /* Safari */
  	backface-visibility: hidden;
	img{
		width:auto;
		height:100%;
	}
}
.verso{
	display: block;
	padding: 16px;
	transform: rotateY(180deg);
	overflow: hidden;
	text-overflow: clip;
	white-space: nowrap;
}
</style>