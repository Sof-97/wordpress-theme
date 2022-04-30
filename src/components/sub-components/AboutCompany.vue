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
					<h4> <i class="fa-solid fa-award"></i>Tradition</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<div class="info">
					<h4> <i class="fa-solid fa-lock"></i>Security</h4>
					<p>
						Lorem ipsum dolor sit amet consectetur adipiscing elit.
					</p>
				</div>
				<div class="info">
					<h4><i class="fa-solid fa-pen-to-square"></i>Certificate</h4>
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
div.about {
	padding: 100px 0;
	background-color: $woodsmoke;
	.section {
		width: 65%;
		margin: 0 auto;
		display: flex;
		& > div {
			width: 50%;
			color: #fff;
		}
		&_left {
            padding-right: 60px;
			h5 {
				color: $fountain-blue;
			}
			h2 {
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
                opacity: 0.8;
				margin: 20px 0;
                line-height: 1.5rem;
			}
		}
		&_right {
			display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            line-height: 1.4rem;
            > *{
                flex-basis: calc(100%/2 - 20px);
            }
            h4{
                font-family: Montserrat;
                font-weight: 700;
                font-size: 1.5rem;
                margin: 20px 0 ;
                i{  
                    color: $fountain-blue;
                    margin-right: 10px;
                }
            }
            p{
                opacity: 0.8;
            }
		}
	}
}
</style>
