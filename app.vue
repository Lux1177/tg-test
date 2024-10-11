<script setup lang="ts">
useHead({
	script: [
		{
			src: 'https://telegram.org/js/telegram-web-app.js',
			defer: true,
		},
	],
})
</script>

<template>
	<div>
		<ClientOnly>
			<div class="app">
				<slot></slot>
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
</style>
