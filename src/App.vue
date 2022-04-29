<template>
	<div id="app">
		<header>
			<HeaderComp :contacts="this.contacts" :menu="menuMainPage"/>
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
				phone: "+1 (305) 1234-5768",
				email: "hello@exampleemail.com",
			},
			menuMainPage: [
				'home',
				'about',
				'services',
				'process',
				'team',
				'blog',
				'get in touch',
			]
		}
	}
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap');

*{
	font-family: Lato ;
	margin: 0;
	box-sizing: border-box;
	padding: 0;
}
</style>
