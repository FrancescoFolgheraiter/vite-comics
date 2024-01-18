<script>
export default{
	data() {
		return{
			text:"-->Content goes here<---",
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
	<main>
		<div class="container">
			<div>
				<h1>
					{{ text }}
				</h1>
			</div>
			<div>
				<ul class="d-flex">
					<li v-for="(elem) in navBar">
						<a href="">
							{{ elem }}
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

</style>
