<template>
	<img alt="Vue logo" src="https://v3.vuejs.org/logo.png" />
	<h1 v-text="title"></h1>
	<p v-html="magic"></p>
</template>


<script>
export default {
	data() {
		return {
			title: 'First Vue 3 app!',
			magic: '<h1>this is a new thing</h1>'
		};
	}
};
</script>





<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
