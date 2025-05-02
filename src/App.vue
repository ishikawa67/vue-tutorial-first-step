<template>
  <div id="app">
    <HelloWorld description="This is a description passed via props!" />
  </div>
</template>

<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue';
</script>

<style>
#app {
  text-align: center;
  margin: 20px;
}
</style>
