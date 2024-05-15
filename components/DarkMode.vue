<template>
	<div class="dark-mode">
		<button
			type="button"
			class="dark:text-gray-300 hover:text-white hover:bg-gray-900 dark:hover:bg-gray-700 dark:hover:text-white rounded-md w-9 text-sm font-medium flex items-center justify-center py-1"
			@click="toggleDark"
		>
			<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 hidden dark:block">
				<path stroke-linecap="round" stroke-linejoin="round" d="M12 3v2.25m6.364.386-1.591 1.591M21 12h-2.25m-.386 6.364-1.591-1.591M12 18.75V21m-4.773-4.227-1.591 1.591M5.25 12H3m4.227-4.773L5.636 5.636M15.75 12a3.75 3.75 0 1 1-7.5 0 3.75 3.75 0 0 1 7.5 0Z" />
			</svg>
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" class="w-6 h-6 block dark:hidden px-1 -rotate-[25deg]">
				<path fill="currentColor" d="M223.5 32C100 32 0 132.3 0 256s100 224 223.5 224c60.6 0 115.5-24.2 155.8-63.4c5-4.9 6.3-12.5 3.1-18.7s-10.1-9.7-17-8.5c-9.8 1.7-19.8 2.6-30.1 2.6c-96.9 0-175.5-78.8-175.5-176c0-65.8 36-123.1 89.3-153.3c6.1-3.5 9.2-10.5 7.7-17.3s-7.3-11.9-14.3-12.5c-6.3-.5-12.6-.8-19-.8z"/>
			</svg>
		</button>
	</div>
</template>

<script setup>
const toggleDark = () => {
    if (document.documentElement.classList.contains('dark')) {
        document.documentElement.classList.remove('dark');
        localStorage.setItem('theme', 'light');
        return;
    }
    document.documentElement.classList.add('dark');
    localStorage.setItem('theme', 'dark');
};
</script>
