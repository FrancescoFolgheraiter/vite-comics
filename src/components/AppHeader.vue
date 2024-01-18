<script>
export default{
	data() {
		return{
			navBar:[
				"CHARACTERS",
				"COMICS",
				"MOVIES",
				"TV",
				"GAMES",
				"COLLECTIBLES",
				"VIDEOS",
				"FANS",
				"NEWS",
				"SHOP"
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
	<header class="debug">
		<div class="container d-flex ">
			<div id="logo">
				<img src="/img/dc-logo.png" alt="">
			</div>
			<nav>
				<ul class="d-flex">
					<li v-for="(elem,i) in navBar">
						<a href="">
							{{ elem }}
						</a>
					</li>
				</ul>
			</nav>
		</div>
	</header>
</template>

<style lang ="scss" scoped>
@use"../assets/scss/main.scss" as *;


</style>
