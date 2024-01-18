<script>
export default{
	data() {
		return{
			text:"-->Content goes here<---"
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
			<h1>
				{{ text }}
			</h1>
		</div>
	</main>
</template>

<style lang ="scss" scoped>
main{
	background-color: grey;
}
.container{
	width:1200px;
	margin:0 auto;
}
</style>
