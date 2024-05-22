<template>
  <div id="app">
    <ParentComponent />
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  name: 'App',
  components: {
    ParentComponent
  }
};
</script>

<style>
/* Tambahkan gaya Anda di sini */
</style>
