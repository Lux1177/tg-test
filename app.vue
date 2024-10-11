<script setup lang="ts">
useHead({
	script: [
		{
			src: 'https://telegram.org/js/telegram-web-app.js',
			defer: true,
		},
	],
})

const { useWebApp, useWebAppRequests } = await import('vue-tg')

const requests = useWebAppRequests()

const getContact = () => {
	requests.requestContact()
}
</script>

<template>
	<div>
		<ClientOnly>
			<div class="app">
				<button @click="getContact">share contact</button>
			</div>
		</ClientOnly>
	</div>
</template>

<style>
.app {
	height: 100vh;
	width: 100vw;
	display: flex;
	justify-content: center;
	align-items: center;
}

button {
	height: 20vh;
	width: 20vw;
	border: 1px solid black;
	padding: 2px;
}
</style>
