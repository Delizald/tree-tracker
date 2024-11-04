<script setup lang="ts">
import Map from './components/Map.vue';
import 'mapbox-gl/dist/mapbox-gl.css'; // Correct import path for Mapbox CSS
</script>

<template>
  <div id="layout">
    <Map />
  </div>
</template>

<style>
#layout {
  display: flex;
  flex: 1;
  position: relative;
  height: 100vh; /* Ensures full height for the map container */
  width: 100vw; /* Ensures full width for the map container */
}
</style>
