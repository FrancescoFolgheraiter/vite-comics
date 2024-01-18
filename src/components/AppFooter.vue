<script>
export default{
	data() {
		return{
			socialIcon:[
			"footer-facebook.png",
			"footer-periscope.png",
			"footer-pinterest.png",
			"footer-twitter.png",
			"footer-youtube.png",
			],
		};
	},
	components:{
		
	},
	methods:{
		getImagePath(imgPath){
			return new URL (imgPath, import.meta.url).href;
		}
	}
}

</script>

<template>
	<footer>
		<div class="container">
			<div class="top-footer d-flex justify-content-between">
				<div id="asideL">
					nav bar
				</div>
				<div id="asideR">
					<img src="/img/dc-logo-bg.png" alt="">
				</div>
			</div>
			<div class="bottom-footer">
				<div>
					<button>
						SING-UP NOW
					</button>
					<div class="social">
						<div>
							FOLLOW US
						</div>
						<div v-for="(elem) in socialIcon" class="social-container">
							<img :src="getImagePath('/img/${elem}')" alt="">
						</div>
					</div>
				</div>
			</div>
		</div>
	</footer>
</template>

<style lang ="scss" scoped>
@use"../assets/scss/main.scss" as *;
footer{
	background-image: url("/img/footer-bg.jpg");

}


</style>
