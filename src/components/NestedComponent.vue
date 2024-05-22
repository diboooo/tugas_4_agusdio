<template>
    <div>
      <h3>HEBAT</h3>
      <ChildComponent @data-emitted="handleDataEmitted"/>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    name: "NestedComponent",
    components: {
      ChildComponent
    },
    methods: {
      handleDataEmitted(data) {
        this.$emit('data-emitted', data);
      }
    }
  };
  </script>
  