<template>
	<div className="header-wrapper">
      <div className="main-logo">
        <h1><strong>Logo</strong></h1>
      </div>
      <div className="header-info">
        <MainMenu />
        <SearchBar />
      </div>
  </div>
</template>

<script>
	import MainMenu from './MainMenu.vue';
	import SearchBar from './SearchBar.vue';
	export default {
		name: 'Header',
		components: {
			MainMenu,
			SearchBar,
		},
	};
</script>

<style>
	.header-wrapper {
		background: #222222;
		color: #ffffff;
		display: flex;
	}
	.header-info {
    width: 80%;
    text-align: right;
	}
</style>
