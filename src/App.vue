<template>
	<div v-for="track in tracks" :key="track.id">
		<Card
			:album="track.album"
			:imageURL="track.image"
			:artist="track.artist"
			:title="track.title"
		/>
	</div>
</template>

<script setup>
import { ref } from 'vue'
import Card from './components/Card.vue'

const tracks = ref([
	{
		id: 1,
		image:
			'https://lastfm.freetls.fastly.net/i/u/300x300/b82ece1a74e59e932a1ca0ea95fd57c5.jpg',
		title: 'Последнее лето',
		artist: 'ssshhhiiittt!',
		album: 'Последнее лето 2',
	},
	{
		id: 2,
		image:
			'https://lastfm.freetls.fastly.net/i/u/300x300/b82ece1a74e59e932a1ca0ea95fd57c5.jpg',
		title: 'Сияние',
		artist: 'ssshhhiiittt!',
		album: 'Последнее лето 2',
	},
	{
		id: 3,
		image:
			'https://lastfm.freetls.fastly.net/i/u/300x300/f313530fbb54c77a3ce0bd5cf63bff0b.jpg',
		title: 'Серф панк',
		artist: 'ssshhhiiittt!',
		album: 'Последнее лето 1',
	},
	{
		id: 4,
		image:
			'https://lastfm.freetls.fastly.net/i/u/300x300/bc0555c16f5e95dee89804ab6eef9458.jpg',
		title: 'Цветы',
		artist: 'ssshhhiiittt!',
		album: 'Третья жизнь',
	},
])
</script>

<style></style>
