<template>
	<h2>
		User <code>id</code> is: {{ $route.params.id }}
	</h2>
</template>

<script>
export default {
	// nuxt specific method, to validate url params
	validate(data) {
		return /^\d+$/.test(data.params.id);
	},
	layout: 'users',
}
</script>

<style>

</style>