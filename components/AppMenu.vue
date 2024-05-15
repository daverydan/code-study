<template>
	<UButton label="Menu" @click="isOpen = true" class="block sm:hidden rounded-sm" />

	<USlideover v-model="isOpen">
		<div class="p-4 flex-1">
			<div class="flex justify-between items-center mb-2">
				<label class="block">Menu</label>
				<UIcon
					  name="i-heroicons-x-mark h-6 w-6 hover:cursor-pointer hover:opacity-75"
					  @click="isOpen = false"
				/>
			</div>

			<UDivider class="mb-4" />

			<menu class="sm:block mr-12">
				<MenuListItems @link-clicked="isOpen = false" />
			</menu>
		</div>
	</USlideover>
</template>

<script setup>
const isOpen = ref(false);
</script>
