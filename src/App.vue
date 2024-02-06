<script setup>
import Cardlist from './components/Cardlistt.vue'
import Header from './components/Header.vue'
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
			<Cardlist />
		</div>
	</div>
</template>

<style scoped></style>
