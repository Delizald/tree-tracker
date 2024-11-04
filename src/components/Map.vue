<template>
  <div ref="mapContainer" class="map-container"></div>
</template>

<script>
import mapboxgl from 'mapbox-gl';

mapboxgl.accessToken = 'REPLACENME';

export default {
  mounted() {
    this.map = new mapboxgl.Map({
      container: this.$refs.mapContainer,
      style: "mapbox://styles/mapbox/streets-v12",
      center: [-71.224518, 42.213995],
      zoom: 9,
      pitch: 60, // 3D effect
      bearing: 0
    });
  },

  unmounted() {
    if (this.map) {
      this.map.remove();
      this.map = null;
    }
  }
};
</script>

<style>
.map-container {
  width: 100%;
  height: 100vh; /* Ensure the map takes up full screen height */
}
</style>
