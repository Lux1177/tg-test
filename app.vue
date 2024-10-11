<script setup lang="ts"></script>

<template>
	<NuxtPage />
	<ClientOnly>
		<MiniApp />
	</ClientOnly>
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
