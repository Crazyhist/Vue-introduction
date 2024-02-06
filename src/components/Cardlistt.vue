<script setup>
import Card from './Card.vue'

const onClickAdded = () => alert('hghfg')
</script>

<template>
	<div class="grid grid-cols-4 gap-5">
		<Card
			title="Мужские Кроссовки Nike Blazer Mid Suede"
			:price="15000"
			imageUrl="/boots-1.jpg"
			:isAdded="true"
			:isFavorite="true"
			:onClickAdded="onClickAdded"
		/>
	</div>
</template>
