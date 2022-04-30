<template>
	<div class="container">
		<div class="row">
			<div class="row_left">
				<h5>WE LIKE WHAT WE DO</h5>
				<h2><span>Team</span> of Experts</h2>
				<p>
					Ethics and integrity are the bases on which our
					professionals build their careers. They are fundamentals
					that become daily attitudes.
				</p>
				<div class="teams">
					<div :key="i" v-for="(item, i) in teamMembers">
						<img :src="require(`../../assets/img${item.img}`)" alt="" />
						<div class="info">
							<h5>{{ item.name }}</h5>
							<h6>{{ item.role }}</h6>
							<div>
								<i class="fa-brands fa-facebook-f"></i>
								<i class="fa-brands fa-twitter"></i>
								<i class="fa-brands fa-linkedin"></i>
							</div>
						</div>
					</div>
				</div>
			</div>
			<div class="row_right">
				<h5>President Speech</h5>
				<p>
					Lorem ipsum dolor sit amet, consectetur adipiscing elit.
					Praesent ut lacinia diam
				</p>
				<p>
					Vivamus efficitur et est quis posuere. Nulla sollicitudin
					vulputate dui, id pretium tortor congue eu. Integer aliquet
					justo eu quam volutpat ullamcorper.
				</p>
				<p>
					Duis ut hendrerit mauris. Phasellus faucibus ut enim vel
					tincidunt. Nunc venenatis a dui et laoreet.
				</p>
				<div>
					<h6>T. Johnson</h6>
					<i class="fa-solid fa-quote-right"></i>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
export default {
	name: "TeamComp",
	props: {
		teamMembers: Array,
	},
};
</script>
<style lang="scss" scoped>
@import "../../style/variables.scss";
div.container {
	background-color: $woodsmoke;
	padding: 80px 0;
	div.row {
		display: flex;
		justify-content: space-between;
		width: 65%;
		margin: 0 auto;
		&_left {
			width: 65%;
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
			.teams {
				color: #fff;
				display: flex;
				justify-content: space-between;
				flex-wrap: wrap;
				margin-top: 30px;
			}
			.teams > div {
				display: flex;
				flex-basis: calc(100% / 2 - 10px);
				margin: 10px 0;
				img {
					height: 120px;
					border-radius: 5px;
					margin-right: 30px;
				}
				.info {
					flex-direction: column;
					h5 {
						font-size: 1.3rem;
						color: #fff;
					}
					h6 {
						font-size: 0.9rem;
						opacity: 0.8;
						margin: 15px 0;
						font-weight: 500;
						text-transform: uppercase;
					}
					div {
						display: flex;
                        i{
                            font-size: 1.2rem;
                            margin: 0 5px;
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            color: $fountain-blue;  
                            border-radius: 50%;
                            background-color: rgba($elf-green, $alpha: 0.4);
                            width: 2.2rem;
                            height: 2.2rem;
                        }
					}
				}
			}
		}
		&_right {
			width: 30%;
			color: #fff;
			background-color: $elf-green;
			border-radius: 8px;
			padding: 25px;
			margin: 2.5rem 0;
			h5 {
				font-size: 1.7rem;
			}
			h6 {
				font-size: 1.2rem;
			}
			p {
				margin: 20px 0;
			}
			div {
				padding: 0 5%;
				display: flex;
				justify-content: space-between;
				i {
					font-size: 2rem;
					color: #000;
					opacity: 0.4;
				}
			}
		}
	}
}
</style>
