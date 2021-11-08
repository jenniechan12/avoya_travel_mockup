<template>
	<b-row align-v="center" align-h="center">
		<b-col cols="12" xl="8">
			<b-row align-v="stretch">
				<Content1 />
				<Content2 />
				<Content3 />
			</b-row>
		</b-col>
	</b-row>
</template>
<script>
import Content1 from './Content1.vue';
import Content2 from './Content2.vue';
import Content3 from './Content3.vue';

export default {
	components: {
		Content1,
		Content2,
		Content3,
	},
};
</script>
