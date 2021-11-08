<template>
	<b-col cols="12" md="4">
		<a id="Tres">
			<div class="text-left m-4">
				<h2>{{ title }}</h2>
				<div class="comment-box-container">
					<div
						class="comment-box"
						v-for="(item, index) in comments"
						:key="index"
					>
						<div>
							<em>"{{ item.comment }}"</em>
						</div>
						<div>
							<b>- {{ showFirstName(item.name) }},</b>
							<span class="ml-2">
								<i class="date"> {{ formatDate(item.timestamp) }} </i>
							</span>
						</div>
					</div>
				</div>
			</div>
		</a>
	</b-col>
</template>
<script>
import json from '../../api/app.json';

export default {
	data() {
		return {
			title: 'What Others Are Saying',
			comments: json,
		};
	},
	beforeMount() {
		this.comments.sort((a, b) => {
			return b.timestamp - a.timestamp;
		});
	},
	methods: {
		formatDate: function (timestamp) {
			let date = new Date(timestamp * 1000);
			const [month, day, year] = [
				date.getMonth() + 1,
				date.getDate(),
				date.getFullYear(),
			];

			return `${month}/${day}/${year}`;
		},
		showFirstName: function (name) {
			return name.split(' ')[0];
		},
	},
};
</script>
<style scoped>
.comment-box-container {
	border: 1px solid #d8d8d8;
}
.comment-box {
	padding: 16px;
	background-color: #d8d8d8;
}
.comment-box:nth-child(odd) {
	background-color: #c5d3e0;
}
.date {
	font-size: 14px;
	font-family: Georgia, 'Times New Roman', Times, serif;
}
</style>
