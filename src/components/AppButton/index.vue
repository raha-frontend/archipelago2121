<template>
	<button
		:type="type"
		:disabled="disabled"
		class="app-button"
	>
		<slot />
	</button>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
	props: {
		theme: {
			type: String,
			default: 'primary' // primary, secondory
		},
		type: {
			type: String,
			default: 'button'
		},
		disabled: {
			type: Boolean,
			default: false
		}
	},
	setup() {
		
	},
})
</script>

<style lang="scss" scoped>
	.app-button {
		padding: 20px 32px;
		font-weight: 500;
		font-size: 24px;
		line-height: 31px;
		border: none;
		background-color: #2185FB;
		border-radius: 130px;
		color: #fff;
		cursor: pointer;
		&:hover {
			background-color: #5ea2f3;
			transition: all 0.3s linear;
		}
	}
</style>
