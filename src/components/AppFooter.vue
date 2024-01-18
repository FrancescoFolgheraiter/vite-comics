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
			comicsList:[
				"Characters",
				"Comics",
				"Movies",
				"TV",
				"Games",
				"Videos",
				"News"
			],
			shopList:[
				"Shop DC",
				"Shop DC collectibles"
			],
			dcList:[
				"Terms Of Use",
				"Privacy policy(New)",
				"Ad Choices",
				"Advertising",
				"Jobs",
				"Subscriptions",
				"Talent Workshops",
				"CPSC Certificates",
				"Ratings",
				"Shop Help",
				"Concact Us"
			],
			siteList:[
				"DC",
				"MAD Magazine",
				"DC Kids",
				"DC Universe",
				"DC Power Visa"
			]
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
			<div class="top-footer  d-flex justify-content-between">
				<div id="asideL d-flex">
					<div>
						<div>
							<h3 class="text-white">DC COMICS</h3>
							<ul>
								<li v-for="(elem) in comicsList">
									{{ elem }}
								</li>
							</ul>
							<h3 class="text-white">SHOP</h3>
							<ul>
								<li v-for="(elem) in shopList">
									{{ elem }}
								</li>
							</ul>
						</div>
					</div>
					<div>
						<h3 class="text-white">
							DC
						</h3>
						<ul>
							<li v-for="(elem) in dcList">
								{{elem}}
							</li>
						</ul>
					</div>
					<div>
						<h3 class="text-white">
							SITES
						</h3>
						<ul>
							<li v-for="(elem) in siteList">
								{{ elem }}
							</li>
						</ul>
					</div>
				</div>
				<div id="asideR">
					<img src="/img/dc-logo-bg.png" alt="">
				</div>
			</div>
			<div class="bottom-footer">
				<div class="d-flex justify-content-between">
					<button>
						SING-UP NOW
					</button>
					<div class="social d-flex">
						<div>
							FOLLOW US
						</div>
						<div class="social-container">
							<img v-for="(elem) in socialIcon" :src="getImagePath('/img/'+ elem)" alt="">
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
.asideL{
	width:50%;
}


</style>
