<template>
	<div class="home">
		<img alt="Vue logo" src="../assets/logo.png" />
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
