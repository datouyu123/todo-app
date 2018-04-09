<template>
	<input 
		type="text" 
		class="my-input" 
		ref="input"
		:value="value"
		@input="$emit('input',$event.target.value)"
		@keydown.enter="$emit('enter')">
</template>
<script>
export default {
	props: {
		value: {
			type: String,
			default: ''
		}
	},
	methods: {
	
	}
}
</script>
<style scoped>
	.my-input {
	  width: 100%;
	  padding: 8px 10px;
	  border: 1px solid #32485F;
	}
</style>