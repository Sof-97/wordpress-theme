<template>
	<div class="container">
		<div class="row">
			<div class="row_left">
				<h5>NEWSLETTER</h5>
				<h2><span>Know</span> First</h2>
				<p>
					Follow closely and receive content about our company and the news of the current market.    
				</p>
			</div>
			<div class="row_right">
				<input type="text" placeholder="Name" />
				<input type="text" placeholder="Email" />
				<button>SUBSCRIBE</button>
			</div>
		</div>
	</div>
</template>
<script>
export default {
	name: "NewsletterComp",
};
</script>
<style lang="scss" scoped>
@import "../../style/variables.scss";
div.container {
	padding: 120px 0;
	background-image: url("../../assets/img/bg-1.jpg");
	background-size: cover;
	background-repeat: no-repeat;
	background-position-y: 30%;
	div.row {
		display: flex;
		justify-content: space-between;
		width: 50%;
		margin: 0 auto;
		&_left {
			width: 60%;
			h5 {
				color: $fountain-blue;
			}
			h2 {
				color: #fff;
				font-family: Poppins;
				font-weight: 700;
				font-size: 4rem;
				margin: 15px 0;
				span {
					background-color: $company;
					border-radius: 5px;
					padding: 5px 10px;
				}
			}
			p {
				color: #fff;
				opacity: 0.8;
			}
		}
		&_right {
			display: flex;
			flex-direction: column;
			width: 35%;
			input {
				width: 100%;
				margin: 10px 0;
				color: rgba(#000, $alpha: 1);
				border-radius: 3px;
				border: 2px solid transparent;
				padding: 13px;
				background-color: rgba($input, $alpha: 0.7);
				&:focus {
					outline: none;
					border: 2px solid $elf-green;
				}
			}
			button {
                display: inline-block;
				color: #fff;
				border: 1px solid $elf-green;
				border-radius: 5px;
				padding: 10px 15px;
				background-color: $elf-green;
                width: fit-content;
				a {
					color: #fff;
					text-decoration: none;
				}
			}
		}
	}
}
</style>
