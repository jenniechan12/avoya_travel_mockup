<template>
	<div id="app">
		<!-- Navigation Bar -->
		<Navbar :links="links" />
		<b-container fluid id="Home">
			<!-- Hero Image Slider -->
			<Hero />

			<!-- Contents -->
			<Contents />
		</b-container>

		<!-- Footer -->
		<Footer :links="links" />
	</div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Contents from './components/contents/Contents.vue';
import Hero from './components/Hero.vue';
import Footer from './components/Footer.vue';

export default {
	name: 'App',
	components: {
		Navbar,
		Hero,
		Contents,
		Footer,
	},
	data() {
		return {
			links: [
				{ href: '#Home', label: 'Home' },
				{ href: '#Uno', label: 'Uno' },
				{ href: '#Dos', label: 'Dos' },
				{ href: '#Tres', label: 'Tres' },
			],
		};
	},
};
</script>

<style>
html {
	overflow-y: auto;
}

body {
	background-color: #dedede;
	margin: 0;
}

#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
}

.img-border {
	border: 4px solid white;
	box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.2);
}
.text-left {
	text-align: left;
}
.text-right {
	text-align: right;
}
</style>
