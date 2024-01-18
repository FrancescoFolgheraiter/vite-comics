<script>
export default{
	data() {
		return{
			navBar:[
				"DIGITAL COMICS",
				"DC MERCHANDISE",
				"SUBSCRIPTION",
				"COMICS SHOP LOCATOR",
				"DC POWE VISA"
			]
		};
	},
	components:{
		
	},
	methods:{

	}
}

</script>

<template>
	<footer>
		<div class="container">
			<div class="top-footer">
				<ul class="d-flex">
					<li v-for="(elem) in navBar">
						<a href="">
							{{ elem }}
						</a>
					</li>
				</ul>
			</div>
			<div class="bottom-footer d-flex">
				<div id="asideL">
					nav bar
				</div>
				<div id="asideR">
					<img src="/img/dc-logo-bg.png" alt="">
				</div>
			</div>
		</div>
	</footer>
</template>

<style lang ="scss" scoped>
.container{
	width:1200px;
	margin:0 auto;
}
ul{
	list-style: none;
}
li{
	margin:auto 10px;
}
.d-flex{
	display:flex;
	flex-wrap: wrap;
}
</style>
