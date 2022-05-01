<template>
	<div class="bg">
		<div class="services">
			<div>
				<h5>OUR BUSINESS AREAS</h5>
				<h2>Excellence in <span>Services</span></h2>
				<div>
					<p>
						We are leaders in providing consultancy services with a
						set of cutting-edge technologies and a team of
						experienced and renowned professionals. These are some
						options that you can hire.
					</p>
					<button><a href="#">SEE ALL</a></button>
				</div>
			</div>
			<div class="cards">
				<!-- Card -->
				<div>
					<div>
						<i class="fa-solid fa-network-wired"></i>
						<i class="fa-solid fa-arrow-right"></i>
					</div>
					<h4>Audit & Assurance</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<!-- Card -->
				<div>
					<div>
						<i class="fa-solid fa-briefcase"></i>
						<i class="fa-solid fa-arrow-right"></i>
					</div>
					<h4>Financial Advisory</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<!-- Card -->
				<div>
					<div>
						<i class="fa-solid fa-chart-simple"></i>
						<i class="fa-solid fa-arrow-right"></i>
					</div>
					<h4>Analytics and M&A</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<!-- Card -->
				<div>
					<div>
						<i class="fa-solid fa-plane-up"></i>
						<i class="fa-solid fa-arrow-right"></i>
					</div>
					<h4>Middle Marketing</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<!-- Card -->
				<div>
					<div>
						<i class="fa-solid fa-earth-europe"></i>
						<i class="fa-solid fa-arrow-right"></i>
					</div>
					<h4>Legal Consulting</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<!-- Card -->
				<div>
					<div>
						<i class="fa-solid fa-inbox"></i>
						<i class="fa-solid fa-arrow-right"></i>
					</div>
					<h4>Regulatory Risk</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
export default {
	name: "ServicesComp",
};
</script>
<style lang="scss" scoped>
@import "../../style/variables.scss";
@import "../../style/mixin.scss";
div.bg {
	background-color: $services;
}
div.services {
	@include container;
	div {
		@include sectionTitle(
			rgba($fountain-blue, $alpha: 0.3),
			$text-color,
			$elf-green
		);
		p {
			color: $lorem;
		}
		button {
			@include button($elf-green);
		}
		div {
			display: flex;
			justify-content: space-between;
			p {
				width: 70%;
			}
		}
	}
}
// Style Cards
div.cards {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-between;
	margin: 20px 0;
	& > div {
		h4 {
			margin: 10px 0 15px 0;
			color: $text-color;
			font-size: 1.4rem;
		}
		div {
			margin-bottom: 15px;
			i {
				&:last-child {
					opacity: 0.5;
					font-size: 1.6rem;
				}
			}
		}
	}
	& > * {
		i {
			font-size: 2rem;
			color: $elf-green;
		}
		display: flex;
		flex-direction: column;
		padding: 40px;
		margin: 20px 0;
		border-radius: 10px;
		background-color: #fff;
		width: calc(100% / 3 - 30px);
		p {
			width: 100% !important;
		}
	}
}
</style>
