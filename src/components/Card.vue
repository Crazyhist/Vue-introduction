<script setup>
defineProps({
	title: String,
	imageUrl: String,
	price: Number,
	isFavorite: Boolean,
	isAdded: Boolean,
	onClickFavorite: Function,
	onClickAdded: Function,
})
</script>

<template>
	<div
		class="relative border border-slate-100 bg-white rounded-3xl p-8 cursor-pointer hover:-translate-y-2 transition hover:shadow-xl"
	>
		<img
			:src="!isFavorite ? '/like-1.svg' : '/like-2.svg'"
			alt="like"
			class="absolute top-8 left-8"
			@click="onClickFavorite"
		/>

		<img :src="imageUrl" alt="" class="" />

		<p class="mt-2">{{ title }}</p>

		<div class="flex justify-between mt-5">
			<div class="flex flex-col">
				<span class="text-slate-400">Цена:</span>
				<b>{{ price }} руб.</b>
			</div>

			<img
				:src="!isAdded ? '/Plus.svg' : '/isCheked.svg'"
				alt="Plus"
				@click="onClickAdded"
			/>
		</div>
	</div>
</template>
