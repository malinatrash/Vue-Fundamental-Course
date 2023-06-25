<script lang="ts">
import { ref } from 'vue'
const count = ref(0)
</script>

<template>
	<div class="flex justify-center items-center w-screen h-screen">
		<h1>{{ count }}</h1>
	</div>
</template>
