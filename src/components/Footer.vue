<template>
	<footer>
		<b-container fluid>
			<b-row align-h="between">
				<b-col class="text-left">
					<span id="Copyright">&copy; Copyright, All Rights Reserved.</span>
				</b-col>
				<b-col class="text-right">
					<div v-if="links.length > 0">
						<a :href="links[0].href" class="links">{{ links[0].label }} </a>
						|
						<a :href="links[1].href" class="links">{{ links[1].label }} </a>
						|
						<a :href="links[2].href" class="links">{{ links[2].label }} </a>
						|
						<a :href="links[3].href" class="links">{{ links[3].label }} </a>
					</div>
				</b-col>
			</b-row>
		</b-container>
	</footer>
</template>
<script>
export default {
	props: {
		links: {
			type: Array,
			default() {
				return [];
			},
		},
	},
};
</script>
<style scoped>
footer {
	background-color: #cccccc;
	padding: 16px 32px;
}
#Copyright {
	font-family: Georgia, 'Times New Roman', Times, serif;
	color: #8c8c8c;
}
.links {
	color: #8c8c8c;
}
</style>
