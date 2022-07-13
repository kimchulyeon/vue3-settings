<template>
	<button @click="add">{{ counter }}</button>
</template>

<script setup>
import { onMounted, ref } from 'vue'

const counter = ref(0)

const add = () => {
	counter.value++
}

onMounted(() => {
	console.log('컴포넌트가 마운트되었습니다::::::::')
})
</script>
