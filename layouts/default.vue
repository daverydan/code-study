<template>
	<div class="max-w-7xl mx-auto p-4">
		<header class="flex space-x-3 sm:space-x-0">
			<AppMenu />
			<AppSearch />
		</header>

		<div class="content flex py-8">
			<AppSidebar />
			<main class="">
				<slot />
			</main>
		</div>

		<footer></footer>
	</div>
</template>
