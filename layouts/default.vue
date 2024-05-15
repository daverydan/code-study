<template>
	<div class="max-w-7xl mx-auto p-4">
		<AppHeader />

		<div class="content flex py-8">
			<AppSidebar />
			<main class="w-full">
				<slot />

				<AppFooter />
			</main>
		</div>
	</div>
</template>
