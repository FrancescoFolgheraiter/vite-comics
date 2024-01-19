<script>
export default{
	data() {
		return{
			
		};
	},
	props:{
		product:Object,
	},
	components:{
		
	},
	methods:{

	}
}

</script>

<template>
	<div>
		<div class="card-product">
			<div class="container-img">
				<img :src="product.thumb" :alt="product.series">
			</div>
			<h3 class="text-white">
				{{ product.series }}
			</h3>
		</div>
	</div>
</template>

<style lang ="scss" scoped>
@use"../assets/scss/main.scss" as *;
.card-product{
	padding: 20px;
	.container-img{
		width: 120px;
		text-align: center;
		img{
			width: 100%;
		}
	}
	h3{
		margin: 20px 0;
	}
}

</style>
