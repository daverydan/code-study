<script setup>
const title = 'Keywords';
const lowercaseTitle = 'keywords';
</script>

<template>
	<div :class="`java page-${lowercaseTitle}`">
		<UBreadcrumb divider="/" :links="[{ label: 'Java', to: '/java' }, { label: title, to: `/java/${lowercaseTitle}` }]" class="mb-4"/>

		<UDivider class="mb-4" />

		<h1 class="text-xl font-bold tracking-wider mb-8">
			{{ title }}
		</h1>

		<p class="leading-8 mb-4">
			A keyword is any one of a number of reserved words, that have a predefined meaning in the Java language.
		</p>
	</div>
</template>
