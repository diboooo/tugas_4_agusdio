<template>
    <div>
      <h2>MAHASISWA/MAHASISWA</h2>
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {
    name: "SlotComponent"
  };
  </script>

<template>
    <div>
      <h1>Parent Component dengan Slot</h1>
      <SlotComponent>
        <p>Ini adalah konten yang disisipkan melalui slot.</p>
        <NestedComponent @data-emitted="displayData"/>
      </SlotComponent>
      <p>Data dari Child: {{ childData }}</p>
    </div>
  </template>
  
  <script>
  import SlotComponent from './SlotComponent.vue';
  import NestedComponent from './NestedComponent.vue';
  
  export default {
    name: "ParentComponent",
    components: {
      SlotComponent,
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
  