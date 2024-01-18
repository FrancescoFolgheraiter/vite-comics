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
	<header class="d-flex debug">
		<div id="logo">
			<img src="/img/dc-logo.png" alt="">
		</div>
		<nav>
			<ul class="d-flex">
				<li v-for="(elem,i) in navBar">
					{{ elem }}
				</li>
			</ul>
		</nav>
	</header>
</template>

<style lang ="scss" scoped>
header{
	width:1200px;
	margin:0 auto;
	justify-content: space-between;
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
