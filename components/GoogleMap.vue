<template>
    <div>
      <div>
        <h2>Search and add a pin</h2>
      </div>
      <br>
      <GmapMap
      :center='center'
      :zoom='12'
      style='width:100%;  height: 400px;'
    />
    </div>
  </template>
  
  <script>
  export default {
    name: 'GoogleMap',
    data() {
        return {
        center: { lat: -6.263303302704724, lng: 107.0293117423296 },
        }
    },
    mounted() {
        this.geolocate();
    },
    methods: {
        geolocate(){
        navigator.geolocation.getCurrentPosition(position => {
            this.center = {
            lat: position.coords.latitude,
            lng: position.coords.longitude,
            };
        });
        },
    },
  }
  </script>