<template>
	<div class="container">
		<!-- Title Section -->
		<div class="title">
			<h5>HOW IT WORKS IN PRACTICE</h5>
			<h2><span>Process</span>Management</h2>
			<p>
				We work with innovative methodologies to ensure that the entire
				reformatting process is done from start to finish as planned.
			</p>
		</div>
		<!-- Timeline Section -->
		<div>
			<div class="timeline">
				<div :key="i" v-for="i in 5">0{{ i }}</div>
			</div>
			<div class="timeline_columns">
				<div>
					<h5>Collection of information</h5>
					<p>Lorem ipsum dolor sit amet consectetur</p>
				</div>
				<div>
					<h5>Strategic planning</h5>
					<p>Lorem ipsum dolor sit amet consectetur</p>
				</div>
				<div>
					<h5>Assignment of responsibilities</h5>
					<p>Lorem ipsum dolor sit amet consectetur</p>
				</div>
				<div>
					<h5>Formatting process</h5>
					<p>Lorem ipsum dolor sit amet consectetur</p>
				</div>
				<div>
					<h5>Continuity formalization</h5>
					<p>Lorem ipsum dolor sit amet consectetur</p>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
export default {
	name: "ManagementComp",
};
</script>
<style lang="scss" scoped>
@import "../../style/variables.scss";
@import "../../style/mixin.scss";
div.container {
    padding: 100px 0;
	div.title {
		text-align: center;
		@include container;
        padding: 0;
		width: 40%;
		@include sectionTitle(
			rgba($fountain-blue, $alpha: 0.3),
			$text-color,
			$elf-green
		);
		p {
			color: $lorem;
		}
	}
	.timeline {
		display: flex;
		justify-content: space-around;
		position: relative;
		height: 5px;
		background-color: $timeline;
		width: 100%;
		margin: 80px 0 20px 0;
		padding: 0 10%;
		div {
			display: flex;
			justify-content: center;
			align-items: center;
			background-color: $timeline;
			border-radius: 50%;
			width: 40px;
			height: 40px;
			position: relative;
			bottom: 15px;
			color: $elf-green;
			font-weight: bolder;
		}
		&_columns {
			display: flex;
			justify-content: space-around;
			padding: 0 10%;
			text-align: center;
			h5 {
				font-size: 1.3rem;
				margin: 15px 0;
				color: $text-color;
			}
			p {
				color: $lorem;
			}
			> div {
				width: calc(100% / 5 - 20px);
			}
		}
	}
}
</style>
