<template>
	<header class="app-header flex justify-between items-center">
		<div class="flex items-center space-x-3">
			<NuxtLink to="/">
				<h1 class="text-lg mr-3 tracking-wide"><span class="font-black">Code</span><span class="font-thin">Study</span></h1>
			</NuxtLink>
			<AppMenu />
			<AppSearch />
		</div>
		<DarkMode />
	</header>
</template>
