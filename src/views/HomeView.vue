<template>
    <div>
      <h1>Canvas to PDF Conversion</h1>
      <CanvasToPdf />
    </div>
  </template>
  
  <script>
  import CanvasToPdf from '../components/CanvasToPdf.vue';
  
  export default {
    name: 'HomeView', // Update the component name here
    components: {
      CanvasToPdf
    }
  }
  </script>
  