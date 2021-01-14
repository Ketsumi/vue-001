<template>
	<h3>{{ title }}</h3>
	<input type="text" ref="name">
	<button @click="handleClick">Do Something</button>
	<div v-show="boxBool">🐸</div>
	<button @click="toggleBox">Toggle</button>
	<Modal v-show="modleBool" />
	<button @click="toggleModal"></button>
</template>

<script>
import Modal from './components/Modal'

export default {
	name: 'App',
	components: { Modal },
	data() {
		return {
			title: 'My First Vue App 😊',
			boxBool: true
		}
	},
	methods: {
		handleClick () {
			console.log(this.$refs.name)
		},
		toggleBox() {
			this.boxBool = !this.boxBool
		}
	}
}
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
