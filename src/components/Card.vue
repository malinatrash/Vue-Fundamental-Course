<template>
	<div class="wrapper">
		<div class="image-wrapper">
			<img class="image" :src="imageURL" :alt="imageURL" />
		</div>
		<h3 class="title">{{ title }}</h3>
		<h5 class="artist">{{ artist }}</h5>
	</div>
</template>

<script setup>
const props = defineProps({
	imageURL: String,
	artist: String,
	album: String,
	title: String,
})
</script>

<style scoped>
.image-wrapper {
	@apply border border-black/70 shadow-lg bg-slate-200 rounded-lg w-64 h-64 transition-all duration-200 hover:w-72 hover:h-72;
}
.wrapper {
	@apply flex-col m-5;
}
.title {
	@apply mt-3 text-center text-4xl;
}
.artist {
	@apply mt-1 text-center text-xl;
}
.image-wrapper img {
	@apply w-full h-auto;
}
</style>
