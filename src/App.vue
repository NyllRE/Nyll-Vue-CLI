<template>
	<img alt="Vue logo" id="vue-logo" src="https://v3.vuejs.org/logo.png" />
	<h1 v-text="title"></h1>
	<p v-html="magic"></p>
	<form @submit.prevent="listing.push({ name: lol })">
		<input class="task-input" v-model="lol" />
		<button class="task-button" type="submit">lol</button>
	</form>
	<ul>
		<li v-for="names in listing">{{ names.name }}</li>
	</ul>
</template>


<script>
export default {
	data() {
		return {
			lol: '',
			title: 'First Vue 3 app!',
			magic: '<h2>this is to-do list</h2>',
			listing: [{ name: 'something' }]
		};
	}
};
</script>





<style>
* {
	padding: 0;
	margin: 0;
}
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	height: 100vh;
	background: linear-gradient(95deg, purple, rgb(255, 118, 140));
}
#vue-logo {
	margin-top: 60px;
	height: 100px;
}
.task-input {
	border: none;
	background: linear-gradient(to left, rgb(109, 0, 128), rgb(173, 102, 114));
	color: wheat;
}
.task-button {
	margin: 5px;
	border: none;
	padding: 5px 15px;
	color: wheat;
	background: linear-gradient(135deg, purple, rgb(255, 30, 67));
}
</style>