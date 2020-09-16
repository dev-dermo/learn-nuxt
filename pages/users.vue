<template>
	<div>
		<input type="text" name="" id="" v-model="userId">
		<button @click="onLoadUser">Load User</button>

		<nuxt-child /> <!-- this loads the users.vue file contents into here, kind of like a partial -->
	</div>
</template>

<script>
export default {
	data() {
		return {
			userId: ''
		};
	},
	methods: {
		onLoadUser() {
			this.$router.push('/users/' + this.userId);
		},
	},
	layout: 'users',
}
</script>

<style>

</style>