<template>
	<img alt="Vue logo" id="vue-logo" src="https://v3.vuejs.org/logo.png" />
	<h1 v-text="title"></h1>
	<p v-html="magic"></p>
	<strong>
		there is {{ taskCount }}
		<span v-if="taskCount == 1"> task </span>
		<span v-else> tasks </span>
	</strong>
	<form @submit.prevent="nigga">
		<input class="task-input" v-model.lazy="lol" />
	</form>
	<ul>
		<li v-for="names in listing" v-bind:key="names">{{ names.name }}</li>
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
	},
	methods: {
		nigga() {
			if (this.lol !== '') {
				this.listing.push({ name: this.lol });
			}
			this.lol = '';
		}
	},
	computed: {
		taskCount() {
			return this.listing.length;
		}
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
</style>