<template>
	<b-col cols="12" md="4" id="Dos">
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
			<ul class="checkmark px-2 py-4">
				<li v-for="(item, index) in list" :key="index">{{ item }}</li>
			</ul>
		</div>
	</b-col>
</template>
<script>
export default {
	data() {
		return {
			title: 'This is Some Content',
			img: 'column-center.jpg',
			alt: 'Content 2 Image',
			list: [
				'Sed lacinia enim et nisl viverra.',
				'Nullam elementum quam in luctus.',
				'Integer ac et lacus hendrerit pretium.',
				'Donec placerate dui et blandit.',
				'Nullam elementum quam in luctus.',
			],
		};
	},
};
</script>
<style>
.checkmark {
	list-style-type: none;
}

.checkmark > li:before {
	content: '\2714';
	margin-right: 8px;
	color: #16c60c;
}
</style>
