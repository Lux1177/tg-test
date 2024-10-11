<script setup lang="ts">
import { useWebAppRequests } from 'vue-tg'
const requests = useWebAppRequests()

const getContact = () => {
	requests.requestContact()
}
</script>

<template>
	<button @click="getContact">share contact</button>
</template>

<style scoped>
button {
	height: 20vh;
	width: 20vw;
	border: 1px solid black;
	padding: 2px;
}
</style>
