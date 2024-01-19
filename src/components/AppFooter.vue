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
		<div class="top-footer">
			<div class="container d-flex">
				<div id="asideL" class="d-flex">
					<div class="col-1">
						<div>
							<h3 class="text-white">DC COMICS</h3>
							<ul>
								<li v-for="(elem,i) in comicsList" :key="i">
									{{ elem }}
								</li>
							</ul>
							<h3 class="text-white">SHOP</h3>
							<ul>
								<li v-for="(elem,i) in shopList" :key="i">
									{{ elem }}
								</li>
							</ul>
						</div>
					</div>
					<div class="col-1">
						<h3 class="text-white">
							DC
						</h3>
						<ul>
							<li v-for="(elem,i) in dcList" :key="i">
								{{elem}}
							</li>
						</ul>
					</div>
					<div class="col-1">
						<h3 class="text-white">
							SITES
						</h3>
						<ul>
							<li v-for="(elem,i) in siteList" :key="i">
								{{ elem }}
							</li>
						</ul>
					</div>
				</div>
				<div id="asideR">

				</div>
			</div>
		</div>
		<div class="bottom-footer">
			<div class="container">
				<div class="d-flex justify-content-between align-items-center">
					<button class="text-white">
						SING-UP NOW
					</button>
					<div class="social d-flex">
						<div>
							FOLLOW US
						</div>
						<div class="social-container">
							<img v-for="(elem,i) in socialIcon" :src="getImagePath('/img/'+ elem)" :alt="elem" :key="i">
						</div>
					</div>
				</div>
			</div>
		</div>
	</footer>
</template>

<style lang ="scss" scoped>
@use"../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as *;
footer{
	min-height: 400px;
	.top-footer{
		background-image: url("/img/footer-bg.jpg");
		background-size: cover;
		background-repeat: no-repeat;
		#asideL{
			width:50%;
			padding: 50px 0;
			.col-1{
				width:33%;

				h3{
					font-weight: bold;
					font-size: 1.5rem;
					margin: 20px 0;
				}
				li{
					color:grey;
					margin-bottom: 5px;
				}
			}
		}
		#asideR{
			width: 50%;
			background-image: url(/img/dc-logo-bg.png);
			background-repeat: no-repeat;
			background-position: center;
			background-size: cover;
		}

	}
	
	.bottom-footer{
		height:80px;
		background-color: $bg-footer;
		vertical-align: middle;
		.container{
			height: 100%;
			> *{
				height: 100%;
			}
		}

		button{
			padding:15px;
			font-weight: bold;
			font-size: 1.5rem;
			border:2px solid $bg-main-bar;
			background-color: transparent;
		}
		.social{

			& >*:first-child{
				color:$bg-main-bar;
				font-size: 1.5rem;
				font-weight: bold;
				margin-right: 40px;
				line-height: 40px;
				vertical-align: middle;
			}
			> .social-container{

				> img{
					margin-right: 20px;
				}
			}
			
		}

	}
}



</style>
