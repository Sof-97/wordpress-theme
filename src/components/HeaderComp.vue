<template>
	<div>
		<!-- Header Top  - orario apertura e contatti -->
		<div class="header_top">
			<div>
				<i style="margin-right: 7px" class="fa-solid fa-clock"></i>
				<span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
			</div>
			<div class="contacts">
				<p><i class="fa-solid fa-phone"></i>{{ contacts.phone }}</p>
				<p><i class="fa-solid fa-envelope"></i>{{ contacts.email }}</p>
				<p>
					<i class="fa-brands fa-facebook-f"></i>
					<i class="fa-brands fa-twitter"></i>
					<i class="fa-brands fa-linkedin"></i>
				</p>
			</div>
		</div>
		<!-- Header Bot - Logo  - Menu Principale -->
		<div class="header_bot" id="menuHeader">
			<div class="logo">
				<p><span>nex</span>gen</p>
			</div>
			<div class="right_side">
				<ul class="menu">
					<li :key="i" v-for="(item, i) in menu">
						<a :href="`#${item.link}`">{{ item.name }}</a>
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "HeaderComp",
	props: {
		contacts: Object,
		menu: Array,
	},
	data() {
		return {
			test: 0,
		};
	},
	created() {
		window.addEventListener("scroll", this.handleScroll);
	},
	destroyed() {
		window.removeEventListener("scroll", this.handleScroll);
	},
	methods: {
		handleScroll(event) {
			console.log(event.path[1].scrollY);
			if(event.path[1].scrollY > 40){
				document.getElementById('menuHeader').classList.add('sticky')
			} else{
				document.getElementById('menuHeader').classList.remove('sticky')
			}
		},
	},
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
@import "../style/mixin.scss";

.header {
	position: relative;
	&_top {
		@media screen and (max-width: 820px) {
			display: none;
		}
		display: flex;
		justify-content: space-around;
		color: rgba($color: #fff, $alpha: 0.7);
		background-color: $text-color;
		padding: 10px 0;
		p {
			margin: 0 10px;
			i {
				margin-right: 7px;
			}
			&:hover {
				color: #fff;
			}
		}
		.contacts {
			display: flex;
			p > i {
				margin: 0 15px;
			}
		}
	}
	&_bot {
		width: 100%;
		position: absolute;
		display: flex;
		justify-content: space-around;
		align-items: center;
		text-transform: uppercase;
		background-color: transparent;
		padding: 10px;
		@media screen and (max-width: 820px) {
			justify-content: start;
			padding: 20px;
		}
		.logo {
			@media screen and (max-width: 820px) {
				margin-left: 10%;
			}
			font-weight: 800;
			letter-spacing: 3px;
			font-size: 1.4rem;
			color: $text-color;
			span {
				color: $fountain-blue;
				background-color: rgba($fountain-blue, $alpha: 0.2);
				padding: 5px 3px 5px 20px;
				border-radius: 20px 0 0 20px;
			}
		}
		.menu {
			@include menu(row);
			margin-right: 100px;
			li {
				@media screen and (max-width: 820px) {
					display: none;
				}
				margin: 0 12px;
				padding: 10px;
				a {
					color: $text-color;
					&:hover {
						color: $elf-green;
					}
				}
				&:last-child {
					background-color: $elf-green;
					border-radius: 5px;
					padding: 10px 15px;
					transition: 0.25s all linear;
					&:hover {
						transform: scale(1.1);
					}
					a {
						color: #fff !important;
					}
				}
			}
		}
	}
}
.sticky{
	position: fixed!important;
	top: 0;
	background-color: #fff;
}
</style>
