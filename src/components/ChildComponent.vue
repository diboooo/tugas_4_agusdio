<template>
    <div>
      <button @click="sendData">Kirim Data ke Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    name: "ChildComponent",
    methods: {
      sendData() {
        this.$emit('data-emitted', 'Data dari Child Component');
      }
    }
  };
  </script>
  