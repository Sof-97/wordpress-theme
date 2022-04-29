<template>
	<div id="app">
		<header>
			<HeaderComp :contacts="contacts"/>
    </header>
		<main>
			<MainComp/>
		</main>
		<footer>
			<FooterComp/>
		</footer>
	</div>
</template>

<script>
import HeaderComp from "./components/HeaderComp.vue"
import MainComp from "./components/MainComp.vue"
import FooterComp from "./components/FooterComp.vue"

export default {
	name: "App",
	components:{
		HeaderComp,
		MainComp,
		FooterComp
	},
	data(){
		return{
			contacts: {
				phone: "0",
				email: "email@testemail.com",
			}
		}
	}
};
</script>

<style lang="scss">

</style>
