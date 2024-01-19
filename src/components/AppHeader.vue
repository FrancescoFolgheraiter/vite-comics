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
	<header>
		<div class="container d-flex align-items-center justify-content-between">
			<div id="logo">
				<img src="/img/dc-logo.png" alt="">
			</div>
			<nav>
				<ul>
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
@use "../assets/scss/partials/variables.scss" as *;
header{
	min-height: 100px;

	nav{
		>ul>li{
			display: inline-block;
			margin: auto 10px;
			a{
				text-decoration: none;
				color:black;
				font-weight: bold;
			}
		}
	}

}

</style>
