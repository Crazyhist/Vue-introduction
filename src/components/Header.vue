<template>
	<header
		class="flex justify-between items-center border-b border-pink-600 px-8 py-8"
	>
		<div class="flex items-center gap-4">
			<img class="w-12" src="/logo.png" alt="logo" />
			<div>
				<h2 class="text-xl font-bold uppercase">Vue project</h2>
				<p class="text-slate-500">Пытка первая</p>
			</div>
		</div>

		<ul class="flex items-center gap-10">
			<li
				class="flex items-center gap-3 text-slate-500 hover:text-black hover:cursor-pointer"
			>
				<img src="/Cart.svg" alt="cart" />
				<span>1488 Крыш.</span>
			</li>

			<li
				class="flex items-center gap-3 text-slate-500 hover:text-black hover:cursor-pointer"
			>
				<img src="/Heart.svg" alt="heart" />
				<span>Закладки</span>
			</li>

			<li
				class="flex items-center gap-3 text-slate-500 hover:text-black hover:cursor-pointer"
			>
				<img src="/Union.svg" alt="profile" />
				<span>Профиль</span>
			</li>
		</ul>
	</header>
</template>
