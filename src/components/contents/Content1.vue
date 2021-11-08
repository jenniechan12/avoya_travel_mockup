<template>
	<b-col cols="12" md="4" id="Uno">
		<div class="text-left m-4">
			<h2>{{ title }}</h2>
			<b-img
				class="img-border"
				:src="require(`../../assets/img/${img}`)"
				fluid-grow
				width="1024"
				height="480"
				:alt="alt"
			/>
			<p class="px-2 py-4">{{ caption }}</p>
		</div>
	</b-col>
</template>
<script>
export default {
	data() {
		return {
			title: 'This is Some Content',
			img: 'column-left.jpg',
			alt: 'Content 1 Image',
			caption:
				'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.',
		};
	},
};
</script>
