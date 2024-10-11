<script lang="ts" setup>
import { MainButton, useWebAppPopup, useWebAppRequests } from 'vue-tg'
import {} from 'vue-tg'
const requests = useWebAppRequests()

const getContact = () => {
	requests.requestContact()
}
</script>

<template>
	<button @click="() => getContact()">Share contact</button>
</template>
