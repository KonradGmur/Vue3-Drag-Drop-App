<template>
	<div class="home">
		<h1>DragDrop</h1>
		<DragDrop />
		<span class="file-info">File: {{ dragdropFile.name }}</span>
	</div>
</template>

<script>
// @ is an alias to /src
import DragDrop from '@/components/DragDrop.vue';
import { ref } from 'vue';

export default {
	name: 'Home',
	components: {
		DragDrop,
	},
	setup() {
		let dragdropFile = ref('');

		return { dragdropFile };
	},
};
</script>

<style lang="scss" scoped>
.home {
	height: 100vh;
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #f1f1f1;
}

h1 {
	font-size: 40px;
	margin-bottom: 32px;
}

.file-info {
	margin-top: 32px;
}
</style>
