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
import data from '@/data.json'

const route = useRoute();
const router = useRouter();

const isOpen = ref(false);

const commandPaletteRef = ref();

const dataListItems = data['data-list-items'];

const groups = computed(() => dataListItems.map(item => ({
	key: item.slug,
	label: item.title,
	inactive: '',
	commands: item.routes,
})))

const routes = dataListItems.map(item => item.routes).flat();

const selected = ref(null);

const getItemEqualToFullPath = (fullPath) => routes.filter(item => item.to === fullPath)[0];

onMounted(() => {
	selected.value = route.fullPath == '/'
		? null
		: getItemEqualToFullPath(route.fullPath);
})

watch(() => selected.value, (newValue) => {
	if (!newValue) return; // accounts for router.afterEach()
	if (newValue.to === route.fullPath) {
		isOpen.value = false;
		return;
	}
	isOpen.value = false;
	router.push(newValue.to);
})

router.afterEach((to, from) => {
	selected.value = getItemEqualToFullPath(to.fullPath)
})
</script>
