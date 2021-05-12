<template>
  <div class="body">
    <Header text="Logo"/>
    <Nav />
    <Article />
    <Sidebar />
    <Footer text="Logo"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Article from './components/Article.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Article,
    Footer,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
