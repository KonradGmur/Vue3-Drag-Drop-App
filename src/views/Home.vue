<template>
	<div class="home">
		<DragDrop />
	</div>
</template>

<script>
// @ is an alias to /src
import DragDrop from '@/components/DragDrop.vue';

export default {
	name: 'Home',
	components: {
		DragDrop,
	},
};
</script>
