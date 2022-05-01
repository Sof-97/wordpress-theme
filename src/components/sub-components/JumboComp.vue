<template>
	<div class="jumbotron">
		<!-- Immagine Grattacielo  -->
		<div class="jumbotron_row">
			<!-- Titolo -->
			<h4>FUSIONS & ACQUISITIONS</h4>
			<h1>
				Insurance <br />
				Consulting
			</h1>
			<!-- Form Contatti -->
			<div class="form">
				<input type="text" placeholder="Name" />
				<input type="text" placeholder="Email" />
				<input type="text" placeholder="Phone" />
				<select name="info" id="info">
					<option value="4">More info</option>
					<option value="1">PlaceHolder1</option>
					<option value="2">PlaceHolder2</option>
					<option value="3">PlaceHolder3</option>
				</select>
			</div>
			<div>
				<button>
					<a href="#"> get in touch </a>
				</button>
				<button>
					<a href="#">read more</a>
				</button>
			</div>
		</div>
	</div>
</template>
<script>
export default {
	name: "JumboComp",
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";
@import "../../style/mixin.scss";

div.jumbotron {
	display: flex;
	align-items: center;
	height: calc(100vh - 40px);
	background-image: url("../../assets/img/bg-6.jpg");
	background-size: cover;
	background-repeat: no-repeat;
	background-position-x: center;
	background-position-y: 50%;
	&_row {
		margin-left: 55%;
		line-height: 3rem;
		h4 {
			margin-left: 10px;
			color: $fountain-blue;
		}
		h1 {
			margin: 20px 10px;
			color: $text-color;
			font-family: Poppins;
			font-weight: 900;
			font-size: 4.5rem;
			line-height: 4.5rem;
		}
		.form {
			display: flex;
			flex-wrap: wrap;
			> * {
				width: calc(35% - 20px);
				margin: 10px;
				color: $cloudy;
				border-radius: 3px;
				border: 2px solid transparent;
				padding: 13px;
				background-color: $input;
				&:focus {
					outline: none;
					border: 2px solid $elf-green;
				}
				option {
					color: rgba($color: #000000, $alpha: 0.7);
				}
			}
			+ div {
				display: flex;
				button {
					@include button($elf-green);
					margin: 10px;
					&:last-child {
						background-color: transparent;
						a {
							color: $elf-green;
						}
					}
				}
			}
		}
	}
}
</style>
