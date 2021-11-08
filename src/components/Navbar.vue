<template>
	<b-navbar toggleable="lg" class="navbar-container">
		<!-- Company's Logo -->
		<b-navbar-brand>
			<img src="../assets/img/logo.png" alt="Logo" />
		</b-navbar-brand>

		<!-- Collapse Menu -->
		<b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

		<b-collapse id="nav-collapse" is-nav>
			<!-- Nav's Button -->
			<b-navbar-nav class="ml-auto">
				<b-button
					class="nav-button"
					v-for="item in links"
					:key="item.href"
					:href="item.href"
				>
					{{ item.label }}

					<!-- <a :href="item.href" style="color: white">
						{{ item.label }}
					</a> -->
				</b-button>
			</b-navbar-nav>
		</b-collapse>
	</b-navbar>
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
.navbar-container {
	background-color: #cccccc;
	border-top: 4px solid #7e7e7e;
	padding: 12px 32px;
}

.buttons-container {
	display: flex;
	width: 20%;
	align-content: center;
	justify-content: center;
	margin: auto 0;
}
.nav-button {
	text-transform: uppercase;
	background-color: #5cc3eb;
	border: 1px solid #5894af;
	color: white;
	padding: 8px;
	width: 100%;
	height: 36px;
	border-radius: 0;
}
</style>
