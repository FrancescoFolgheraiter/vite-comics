<script>
//importazione app
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbotron from './components/AppJumbotron.vue';

export default{
	data() {
		return{

		};
	},
	components:{
		AppHeader,
		AppMain,
		AppFooter,
		AppJumbotron,
	},
	methods:{

	}
}

</script>

<template>
	<AppHeader/>
	<AppJumbotron/>
	<AppMain/>
	<AppFooter/>
</template>

<style lang="scss">
@use"assets/scss/main.scss" as *;
@import "assets/scss/partials/reset.scss";
</style>
