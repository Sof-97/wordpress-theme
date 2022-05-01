<template>
	<div>
		<div class="footer_top">
			<div class="container">
				<div class="contacts">
					<div>
						<div class="logo">
							<p><span>nex</span>gen</p>
						</div>
						<p>
							A Functional HTML Template for Corporate & Business.
						</p>
					</div>
					<div>
						<p>
							<i class="fa-solid fa-phone"></i
							>{{ contacts.phone }}
						</p>
						<p>
							<i class="fa-solid fa-envelope"></i
							>{{ contacts.email }}
						</p>
						<p>
							<i class="fa-solid fa-location-dot"></i
							>{{ contacts.address }}
						</p>
					</div>
					<button>
						<a href="#"> get in touch </a>
					</button>
				</div>
				<div class="menu">
					<div>
						<h4>About</h4>
						<ul>
							<li :key="i" v-for="(item, i) in menuFooterAbout">
								<i class="fa-solid fa-chevron-right"></i>
								{{ item }}
							</li>
						</ul>
					</div>
					<div>
						<h4>Services</h4>
						<ul>
							<li
								:key="i"
								v-for="(item, i) in menuFooterServices"
							>
								<i class="fa-solid fa-chevron-right"></i>
								{{ item }}
							</li>
						</ul>
					</div>
					<div>
						<h4>Support</h4>
						<ul>
							<li :key="i" v-for="(item, i) in menuFooterSupport">
								<i class="fa-solid fa-chevron-right"></i>
								{{ item }}
							</li>
						</ul>
					</div>
				</div>
			</div>
		</div>
		<div class="footer_bot">
			<p>Enjoy the low price. We are tracking any intention of piracy.</p>
			<p>© 2021 NEXGEN is Proudly Powered by <a href="#">Gerardo</a>.</p>
		</div>
	</div>
</template>
<script>
export default {
	name: "FooterComp",
	props: {
		menuFooterAbout: Array,
		menuFooterServices: Array,
		menuFooterSupport: Array,
		contacts: Object,
	},
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
@import "../style/mixin.scss";
div.footer {
	&_top {
		background-color: $woodsmoke;
		padding: 100px 0;
		div.container {
			display: flex;
			justify-content: space-between;
			@media screen and (max-width: 820px) {
				flex-direction: column;
			}
			width: 65%;
			margin: 0 auto;
			color: #fff;
			@media screen and (max-width: 820px) {
				width: 80%;
			}
			.contacts {
				display: flex;
				flex-direction: column;
				@media screen and (max-width: 820px) {
					flex-direction: row;
					justify-content: space-between;
					width: 100%;
				}
				@media screen and (max-width: 400px) {
					flex-wrap: wrap;
				}
				width: 30%;
				padding: 30px 30px 30px 0;
				.logo {
					padding: 0;
					text-transform: uppercase;
					font-weight: 800;
					letter-spacing: 3px;
					font-size: 1.4rem;
					span {
						color: $elf-green;
						background-color: rgba($elf-green, $alpha: 0.2);
						padding: 5px 3px 5px 20px;
						border-radius: 20px 0 0 20px;
					}
				}
				p {
					opacity: 0.7;
					margin: 10px 0;
					&:nth-child(2) {
						margin: 30px 0;
					}
					&:nth-child(1) {
						opacity: 1;
					}
					i {
						margin-right: 15px;
					}
				}
				button {
					@include button(transparent);
					height: fit-content;
				}
			}
			.menu {
				width: 70%;
				display: flex;
				@media screen and (max-width: 400px) {
					flex-direction: column;
				}
				justify-content: space-between;
				@media screen and (max-width: 820px) {
					width: 100%;
				}
				div {
					background-color: rgba($color: #fff, $alpha: 0.05);
					border-radius: 10px;
					padding: 40px;
					display: flex;
					flex-direction: column;
					width: calc(100% / 3 - 20px);
					margin: 10px 0;
					@media screen and (max-width: 820px) {
						width: calc(100% / 3 - 5px);
						margin: 5px 0;
					}
					@media screen and (max-width: 400px) {
						width: 100%;
					}
					ul {
						@include menu(column);
						li {
							opacity: 0.7;
							i {
								margin-right: 1rem;
							}
							margin: 0.5rem 0;
						}
					}
					h4 {
						font-size: 1.5rem;
						margin-bottom: 20px;
					}
				}
			}
		}
	}
	&_bot {
		padding: 0 10%;
		background-color: $footer-bot;
		display: flex;
		justify-content: space-around;
		color: #fff;
		p {
			font-size: 0.9rem;
			opacity: 0.6;
			padding: 20px 0;
			a {
				color: $fountain-blue;
				text-decoration: none;
			}
		}
	}
}
</style>
