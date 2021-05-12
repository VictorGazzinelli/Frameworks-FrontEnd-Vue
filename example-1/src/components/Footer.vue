<template>
	<footer class="footer">
			<h1 id="title">{{ text }}</h1>
	</footer>
</template>

<script>
	export default {
		name: 'Footer',
		props: {
			text: String,
		},
	};
</script>

<style>
	.footer {
		background: #222222;
		color: #ffffff;
		text-align:left;
	}

	#title{
		margin: 0;
	}
</style>
