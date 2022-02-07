<template>
  <div id="app">
    <TheHeader class="header"></TheHeader>
    <main class="main">
      <h1>Hello, bloggr</h1>
    </main>
    <TheFooter class="footer"></TheFooter>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  name: 'App',
  components: { TheHeader, TheFooter },
};
</script>

<style lang="scss" scoped>

</style>
