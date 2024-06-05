<script setup>
//
</script>

<template>
	<div class="page-php">
		<UBreadcrumb divider="/" :links="[{ label: 'Patterns & Principles', to: '/patterns-principles' }]" class="mb-4" />

		<UDivider class="mb-4" />

		<h1 class="text-xl font-bold tracking-wider mb-8">
			Start Patterns & Principles
		</h1>

		<p class="leading-8 mb-2"><strong>SOLID</strong> principles</p>
		<UDivider class="mb-2" />
		<p class="mb-2">Resources:</p>
		<ul class="list-disc ml-5 space-y-1">
			<li>
				<a href="https://www.freecodecamp.org/news/solid-principles-explained-in-plain-english/" class="text-primary-400 hover:text-primary-500 transition-all duration-200 hover:underline underline-offset-4">
					Solid Principles Explained in Plain English
				</a>
			</li>
		</ul>
	</div>
</template>
