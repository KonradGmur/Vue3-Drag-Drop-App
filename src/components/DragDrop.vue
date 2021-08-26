<template>
	<div
		@dragenter.prevent="toggleActive"
		@dragleave.prevent="toggleActive"
		@dragover.prevent
		@drop.prevent="toggleActive"
		:class="{ 'active-drop': active }"
		class="dragdrop"
	>
		<span>Drag or Drop File</span>
		<span>OR</span>
		<label for="dragdropFile">Select File</label>
		<input type="file" id="dragdropFile" class="dragdropFile" />
	</div>
</template>

<script>
import { ref } from 'vue';
export default {
	name: 'DragDrop',
	setup() {
		const active = ref(false);

		const toggleActive = () => {
			active.value = !active.value;
		};

		return { active, toggleActive };
	},
};
</script>

<style scoped lang="scss">
.dragdrop {
	width: 400px;
	height: 200px;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	row-gap: 16px;
	border: 2px dashed #41b883;
	background-color: #fff;
	transform: 0.3s ease all;

	label {
		padding: 8px 12px;
		color: #fff;
		background-color: #41b883;
		transform: 0.3s ease all;
	}

	input {
		display: none;
	}
}

.active-drop {
	color: #fff;
	border-color: #fff;
	background-color: #41b883;

	label {
		background-color: #fff;
		color: #41b883;
	}
}
</style>
