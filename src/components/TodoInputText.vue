<template>
	<input 
		type="text" 
		class="my-input" 
		ref="input"
		:value="value"
		@input="updateValue($event.target.value)">
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
		updateValue (value) {
			
			//触发父组件input事件
			this.$emit('input',value)
		}
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