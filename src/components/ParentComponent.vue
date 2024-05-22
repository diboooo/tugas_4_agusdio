<template>
    <div>
      <h1>KAMPUS MERDEKA</h1>
      <NestedComponent @data-emitted="displayData"/>
      <p>Data dari Child: {{ childData }}</p>
    </div>
  </template>
  
  <script>
  import NestedComponent from './NestedComponent.vue';
  
  export default {
    name: "ParentComponent",
    components: {
      NestedComponent
    },
    data() {
      return {
        childData: ''
      };
    },
    methods: {
      displayData(data) {
        this.childData = data;
      }
    }
  };
  </script>
  