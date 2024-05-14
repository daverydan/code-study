<template>
	<aside class="hidden sm:block mr-12">
		<NuxtLink to="/java" class="block mb-2">Java</NuxtLink>
		<UVerticalNavigation
			class="mb-4"
			:links="utilsListItems.java"
			:ui="ui"
		/>

		<NuxtLink to="/php" class="block mb-2">PHP</NuxtLink>
		<UVerticalNavigation
			class="mb-4"
			:links="utilsListItems.php"
			:ui="ui"
		/>

		<NuxtLink to="/javascript" class="block mb-2">JavaScript</NuxtLink>
		<UVerticalNavigation
			class="mb-4"
			:links="utilsListItems.javascript"
			:ui="ui"
		/>

		<NuxtLink to="/sql" class="block mb-2">SQL</NuxtLink>
		<UVerticalNavigation
			class="mb-4"
			:links="utilsListItems.sql"
			:ui="ui"
		/>
	</aside>
</template>

<script setup>
const ui = {
	wrapper: 'border-s border-gray-200 dark:border-gray-800 space-y-2',
	base: 'group block border-s -ms-px leading-6 before:hidden',
	padding: 'p-0 ps-4',
	rounded: '',
	font: '',
	ring: '',
	active: 'text-primary-500 dark:text-primary-400 border-current font-semibold',
	inactive: 'border-transparent hover:border-gray-400 dark:hover:border-gray-500 text-gray-700 hover:text-gray-900 dark:text-gray-400 dark:hover:text-gray-300'
};
</script>
