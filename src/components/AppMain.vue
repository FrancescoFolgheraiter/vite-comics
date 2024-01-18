<script>
export default{
	data() {
		return{
			text:"-->Content goes here<---",
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
	<main>
		<div class="container">
			<div>
				<h1>
					{{ text }}
				</h1>
			</div>
			<div>
				<ul class="d-flex">
					<li v-for="(elem) in navBar" class="d-flex">
						<div class="img-container">
							<img :src="getImagePath(elem.path)"  alt="">
						</div>
						<a href="">
							{{ elem.name }}
						</a>
					</li>
				</ul>
			</div>
		</div>
	</main>
</template>

<style lang ="scss" scoped>
@use"../assets/scss/main.scss" as *;
main{
	background-color: grey;
}
.img-container{
	max-width: 80px;
	height: 90px;
	
	> img{
    width: 100%;
	height: 100%;
	object-fit: cover;
	}
}

</style>
