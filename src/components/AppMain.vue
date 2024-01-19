<script>
import AppBlueBarMain from './AppBlueBarMain.vue';

export default{
	data() {
		return{
			text:"-->Content goes here<---",
			
		};
	},
	components:{
		AppBlueBarMain,
	},
	methods:{
		getImagePath(imgPath){
			return new URL (imgPath, import.meta.url).href;
		}
	}
}

</script>

<template>
	<main>
		<div class="container">
			<div>
				<h1 class="text-white">
					{{ text }}
				</h1>
			</div>
		</div>
		<AppBlueBarMain/>
	</main>
</template>

<style lang ="scss" scoped>
@use"../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as *;
main{
	background-color: $bg-main;
	.img-container{
		max-width: 80px;
		height: 90px;
		
		> img{
		width: 100%;
		height: 100%;
		object-fit: cover;
		}
	}
}

</style>
