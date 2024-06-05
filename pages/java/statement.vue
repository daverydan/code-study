<script setup>
//
</script>

<template>
	<div class="java page-statement">
		<UBreadcrumb divider="/" :links="[{ label: 'Java', to: '/java' }, { label: 'Statement', to: '/java/statement' }]" class="mb-4"/>

		<UDivider class="mb-4" />

		<h1 class="text-xl font-bold tracking-wider mb-8">Statement</h1>

		<p class="leading-8 mb-4">
			A statement is a complete command to be executed that can include one or more expressions.
		</p>

		<p class="mb-2 italic">Example:</p>
		<code>
			System.out.print("Hello World");
		</code>
	</div>
</template>
