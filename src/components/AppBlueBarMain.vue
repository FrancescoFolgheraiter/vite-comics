<script>
export default{
	data() {
		return{
			navBar:[
				{
					name:"DIGITAL COMICS",
					path:"/img/buy-comics-digital-comics.png"
				},
				{
					name:"DC MERCHANDISE",
					path:"/img/buy-comics-merchandise.png"
				},
				{
					name:"SUBSCRIPTION",
					path:"/img/buy-comics-subscriptions.png"
				},
				{
					name:"COMICS SHOP LOCATOR",
					path:"/img/buy-comics-shop-locator.png"
				},
				{
					name:"DC POWE VISA",
					path:"/img/buy-dc-power-visa.svg"
				}
				
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
	<div class="bar-Dc ">
		<div class="container-small d-flex">
			<div class="col-1-5 align-items-center" v-for="(elem,i) in navBar" :key="i">
					<div class="img-container">
						<img :src="getImagePath(elem.path)"  :alt="elem.name">
					</div>
					<a href="">
						{{ elem.name }}
					</a>
			</div>
		</div>
	</div>
</template>

<style lang ="scss" scoped>
@use"../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as *;
.bar-Dc{
	padding: 30px 0;
	background-color: $bg-main-bar;
	.col-1-5{
		display: flex;
		flex-wrap: wrap;;
		.img-container{
			width:50px;
			img{
				width:100%
			}
		}
		a{
			color:white;
			text-decoration: none;
			margin: 0 10px;
		}
	}
}

</style>
