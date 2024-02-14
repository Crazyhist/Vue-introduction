<script setup>
import { onMounted, ref } from 'vue'
import axios from 'axios'

import Cardlist from './components/Cardlistt.vue'
import Drawer from './components/Drawer.vue'
import Header from './components/Header.vue'

const items = ref([]) // items - { }, { value: []}

onMounted(async () => {
	try {
		const { data } = await axios.get(
			'https://e5710d9d6f5ebd34.mokky.dev/items-vue'
		)

		items.value = data
		console.log(data)
	} catch (e) {
		console.log(err)
	}
})
</script>

<template>
	<div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
		<!-- <Drawer /> -->
		<Header />

		<div class="p-10">
			<div class="flex justify-between items-center">
				<h2 class="text-3xl font-bold mb-8">Все кроссовки</h2>
				<div class="flex gap-4">
					<select
						class="py-2 px-3 border border-gray-200 rounded-md outline-none"
						id=""
					>
						<option value="">По названию</option>
						<option value="">По цене (дешевые)</option>
						<option value="">По цене (дорогие)</option>
					</select>
					<div class="relative">
						<img class="absolute left-3 top-3" src="/Search.svg" alt="" />
						<input
							class="border border-gray-200 rounded-md py-2 pl-11 pr-4 outline-none focus:border-gray-400"
							type="text"
							placeholder="Поиск"
						/>
					</div>
				</div>
			</div>
			<Cardlist :items="items" />
		</div>
	</div>
</template>

<style scoped></style>
