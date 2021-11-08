<template>
	<b-row class="justify-content-center">
		<b-col cols="12" xl="8">
			<b-carousel
				id="heroSlide"
				v-model="slide"
				:interval="4000"
				class="m-4 img-border"
				background="#7e7e7e"
				img-width="1024"
				img-height="480"
				@sliding-start="onSlideStart"
				@sliding-end="onSlideEnd"
			>
				<b-carousel-slide
					v-for="(item, index) in images"
					:key="index"
					:img-src="require(`../assets/img/slideshow/${item.name}`)"
					:img-alt="item.alt"
				>
				</b-carousel-slide>
			</b-carousel>
		</b-col>
	</b-row>
</template>
<script>
export default {
	data() {
		return {
			slide: 0,
			sliding: null,
			images: [
				{ name: '1.jpg', alt: 'Image 1' },
				{ name: '2.jpg', alt: 'Image 2' },
				{ name: '3.jpg', alt: 'Image 3' },
			],
		};
	},
	methods: {
		onSlideStart: function () {
			this.sliding = true;
		},
		onSlideEnd: function () {
			this.sliding = false;
		},
	},
};
</script>
