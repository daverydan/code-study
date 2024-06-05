<template>
	<div class="menu-list-items">
		<template v-for="items in data['data-list-items']" :key="items.title">
			<NuxtLink
				to="/patterns-principles"
				class="block mb-2"
			>
				{{ items.title }}
			</NuxtLink>
			<UVerticalNavigation
				class="mb-4"
				:links="items.routes"
				:ui="ui"
				@click="$emit('link-clicked')"
			/>
		</template>
	</div>
</template>

<script setup>
import data from '@/data.json'

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
