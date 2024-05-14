<template>
	<div class="app-search">
		<UButton
			@click="isOpen = true"
			class="rounded-sm"
			label="Search"
		/>

		<UModal v-model="isOpen">
			<UCommandPalette
				ref="commandPaletteRef"
				v-model="selected"
				:autoselect="false"
    			:groups="groups"
				:close-button="{ icon: 'i-heroicons-x-mark-20-solid', color: 'gray', variant: 'link', padded: false }"
			/>
		</UModal>
	</div>
</template>

<script setup>
const route = useRoute();
const router = useRouter();

const isOpen = ref(false);

const commandPaletteRef = ref();

const groups = [{
	key: 'java',
	label: 'Java',
	inactive: '',
	commands: utilsListItems.java,
}, {
	key: 'javascript',
	label: 'Javascript',
	inactive: '',
	commands: utilsListItems.javascript,
}]

const selected = ref([utilsListItems.java[0]]);

watch(() => selected.value, (newValue) => {
	if (newValue.url === route.fullPath) {
		isOpen.value = false;
		return;
	}
	isOpen.value = false;
	router.push(newValue.url);
})
</script>
