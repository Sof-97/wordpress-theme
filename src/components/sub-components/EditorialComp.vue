<template>
	<div class="container">
		<div class="row">
			<div>
				<h5>OUR EDITORIAL CONTENT</h5>
				<h2>Latest <span>News</span></h2>
				<div>
					<p>
						Every week we publish content about what is best in the
						business world.
					</p>
					<button><a href="#">SEE ALL</a></button>
				</div>
			</div>
			<div class="editorials" v-dragscroll="true">
				<div
					:key="i"
					v-for="(item, i) in newsData"
					:style="{
						backgroundImage: `url(${require('@/assets/img' +
							item.img)})`,
					}"
				>
					<h4>{{ item.title }}</h4>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
// Libreria che permette il grab and scroll
import { dragscroll } from "vue-dragscroll";
export default {
	name: "EditorialComp",
	props: {
		newsData: Array,
	},
	directives: {
		dragscroll,
	},
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";
@import "../../style/mixin.scss";
div.container {
	background-color: #fff;
	div.row {
		@include container;
		div {
			@include sectionTitle(
				rgba($fountain-blue, $alpha: 0.3),
				$text-color,
				$elf-green
			);
			p {
				color: $lorem;
				display: flex;
				align-items: center;
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
		.editorials {
			display: flex;
			justify-content: space-between;
			overflow-x: auto;
			margin-top: 30px;
			&::-webkit-scrollbar {
				display: none;
			}
			div {
				text-align: center;
				cursor: grab;
				min-width: calc(100% / 3 - 20px);
				height: calc((((100vw) / 100) * 65) / 3 - 20px);
				margin: 0 10px;
				border-radius: 15px;
				background-size: cover;
				background-position: center;
				display: flex;
				justify-content: center;
				align-items: flex-end;
				padding: 40px;
				background-color: rgba(#fff, $alpha: 1);
				h4 {
					font-size: 1.5rem;
					color: #fff;
				}
			}
		}
	}
}
</style>
