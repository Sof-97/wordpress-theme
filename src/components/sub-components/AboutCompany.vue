<template>
	<div class="about">
		<div class="section">
			<div class="section_left">
				<h5>ABOUT THE NETWORK</h5>
				<h2>
					<span>The</span>
					Company
				</h2>
				<p>
					Lorem ipsum dolor sit amet, consectetur adipiscing elit.
					Cras iaculis diam varius diam ultricies lacinia. Mauris
					lacus tellus, ultrices eu volutpat sit amet, finibus a
					ipsum.
				</p>
				<p>
					Curabitur convallis, diam a egestas iaculis, neque lorem
					interdum felis, in viverra lacus tortor in leo.
				</p>
			</div>
			<div class="section_right">
				<div class="info">
					<h4><i class="fa-solid fa-award"></i>Tradition</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<div class="info">
					<h4><i class="fa-solid fa-lock"></i>Security</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<div class="info">
					<h4>
						<i class="fa-solid fa-pen-to-square"></i>Certificate
					</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<div class="info">
					<h4><i class="fa-solid fa-graduation-cap"></i>Expertise</h4>
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
	name: "AboutCompany",
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";
@import "../../style/mixin.scss";
div.about {
	background-color: $woodsmoke;
	.section {
		@include container;
		display: flex;
		@media screen and (max-width: 400px){
			flex-direction: column;
			}
		& > div {
			width: 50%;
			color: #fff;
			@media screen and (max-width: 400px){
				width: 90%;
			}
		}
		&_left {
			padding-right: 60px;
			@include sectionTitle(rgba($elf-green, 0.2), #fff, #fff);
			p {
				margin: 20px 0;
				line-height: 1.5rem;
			}
		}
		&_right {
			display: flex;
			flex-wrap: wrap;
			justify-content: space-between;
			@media screen and (max-width: 820px){
				justify-content: space-around;
			}	
			line-height: 1.4rem;
			> * {
				flex-basis: calc(100% / 2 - 20px);
			}
			h4 {
				font-size: 1.5rem;
				margin: 20px 0;
				i {
					color: $fountain-blue;
					margin: 10px;
				}
			}
		}
	}
	p {
		opacity: 0.8;
	}
}
</style>
