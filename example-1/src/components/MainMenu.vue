<template>
  <ul :class="$style.list">
    <li :class="$style.item"><a href="/#top1">Topico 1</a></li>
    <li :class="$style.item"><a href="/#top2">Topico 2</a></li>
    <li :class="$style.item"><a href="/#top3">Topico 3</a></li>
    <li :class="$style.item"><a href="/#top4">Topico 4</a></li>
  </ul>
</template>

<script>
	export default {
		name: 'MainMenu',
	};
</script>

<style module lang="scss">
	.list {
      list-style: none;

      li {
        display: inline-block;
        margin-right: 16px;

        a {
          text-decoration: none;
          color: white;
        }
      }
  }
</style>
