<template>
	<div id="app">
		<header id="#home">
			<HeaderComp :contacts="contacts" :menu="menuMainPage" />
		</header>
		<main>
			<MainComp :teamMembers="teamMembers" :newsData="newsData" />
		</main>
		<footer>
			<FooterComp
				:contacts="contacts"
				:menuFooterAbout="menuFooterAbout"
				:menuFooterServices="menuFooterServices"
				:menuFooterSupport="menuFooterSupport"
			/>
		</footer>
	</div>
</template>

<script>
	import HeaderComp from "./components/HeaderComp.vue";
	import MainComp from "./components/MainComp.vue";
	import FooterComp from "./components/FooterComp.vue";

	export default {
		name: "App",
		components: {
			HeaderComp,
			MainComp,
			FooterComp,
		},
		data() {
			return {
				contacts: {
					phone: "+1 (305) 1234-5768",
					email: "hello@exampleemail.com",
					address: "Main Avenue, 987",
				},
				menuMainPage: [
					{
						name: "home",
						link: "app",
					},
					{
						name: "about",
						link: "about",
					},
					{
						name: "services",
						link: "services",
					},
					{
						name: "process",
						link: "process",
					},
					{
						name: "team",
						link: "team",
					},
					{
						name: "blog",
						link: "blog",
					},
					{
						name: "get in touch",
						link: "app",
					},
				],
				teamMembers: [
					{
						name: "David Cooper",
						role: "cto & co-founder",
						img: "/team-1.jpg",
					},
					{
						name: "Oliver Jones",
						role: "chief procurement",
						img: "/team-3.jpg",
					},
					{
						name: "Emma Lopez",
						role: "chief marketing",
						img: "/team-2.jpg",
					},
					{
						name: "T. Johnson",
						role: "ceo & president",
						img: "/team-4.jpg",
					},
				],
				newsData: [
					{
						title: "Increasing creativity is possible for everyone",
						img: "/news-1.jpg",
					},
					{
						title: "Because market research is part of the business plan",
						img: "/news-2.jpg",
					},
					{
						title: "Working from home is now a trend",
						img: "/news-3.jpg",
					},
					{
						title: "PlaceHolder 1",
						img: "/news-4.jpg",
					},
					{
						title: "PlaceHolder 2",
						img: "/news-5.jpg",
					},
				],
				menuFooterAbout: [
					"The Company",
					"Institutional",
					"Social & Events",
					"Innovation",
					"Environment",
					"Technology",
				],
				menuFooterServices: [
					"Audi & Assurance",
					"Financial Advisory",
					"Analytics M&A",
					"Middle Marketing",
					"Legal Consulting",
					"Regulatory Risk",
				],
				menuFooterSupport: [
					"Responsibility",
					"Terms of Use",
					"About Cookies",
					"Privacy Policy",
					"Accessibility",
					"Information",
				],
			};
		},
	};
</script>

<style lang="scss">
	@import url("https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500;1,600;1,700&family=Poppins:wght@700;900&display=swap");
	header{
		z-index: 10;
	}
	* {
		font-family: Montserrat;
		margin: 0;
		box-sizing: border-box;
		padding: 0;
	}
</style>
