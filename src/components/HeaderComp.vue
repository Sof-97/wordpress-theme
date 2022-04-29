<template>
	<div>
		<!-- Header Top  - orario apertura e contatti -->
		<div class="header_top">
			<div>
				<i class="fa-solid fa-clock"></i>
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
		<div class="header_bot">
			<div class="logo">
				<p><span>nex</span>gen</p>
			</div>
			<div class="right_side">
				<ul class="menu">
					<li :key="i" v-for="(item, i) in menu">
						<a href="#">{{ item }}</a>
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
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
@import "../style/mixin.scss";

.header {
	&_top {
		display: flex;
		justify-content: space-around;
		color: #fff;
		background-color: $text-color;
		padding: 5px 0;
		i {
			margin-right: 5px;
		}
		.contacts {
			display: flex;
		}
	}
	&_bot {
		display: flex;
		justify-content: space-around;
		align-items: center;
		text-transform: uppercase;
		padding: 10px;
		background-color: $jumbo-white;
		.logo {
            font-weight: 800;
            letter-spacing: 3px;
            span {
				color: $fountain-blue;
				background-color: rgba($fountain-blue, $alpha: 0.2);
				padding: 5px 3px 5px 20px;
				border-radius: 20px 0 0 20px;
			}
		}
		.menu {
			@include menu(row);

			li {
				margin: 0 8px;
				padding: 10px;
				a {
					color: $text-color;
				}
				&:last-child {
					background-color: $elf-green;
					border-radius: 5px;
					padding: 10px 15px;
					a {
						color: #fff !important;
					}
				}
			}
		}
	}
}
</style>
