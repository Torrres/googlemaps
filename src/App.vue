<template>
  <div>
    <GmapMap :center="{lat:23, lng:10}"
    :zoom="2" map-type-id="terrain"
    style="width: 500px; height: 500px"
    >

      <GmapMarker :key="index" v-for="(m, index) in markers"
      :position="m.position" :clickable="true"
      :draggable="true"
      @click="center=m.position"

      />


    <gmap-custom-marker :marker="mark.position" v-for="(mark, index) in markers">
    <img src="https://www.maven.com/content/dam/maven/consumer/united-states/mavenhome/maven-cars-around-corner-six-icons.png" />
    </gmap-custom-marker>
    </GmapMap>
  </div>
</template>

<script>
  import Vue from 'vue'
  import * as VueGoogleMaps from 'vue2-google-maps'
  import GmapCustomMarker from 'vue2-gmap-custom-marker';
  Vue.use(VueGoogleMaps, {
    load: {
      key: 'AIzaSyD2E7tD7AntATLqyEHkvgpJCqHeRVX4HPA',
      libraries: 'places', // This is required if you use the Autocomplete plugin
    }
  })


  export default {
    name: 'App',
    data() {
      return {
        valor: 2,
        markers: [{
            position: {
              lat: 10.0,
              lng: 10.0
            }
          }, {
            position: {
              lat: 11.0,
              lng: 11.0
            }
          }]
      }
    },
    components:{
      GmapCustomMarker
    }
  }
</script>

<style>
  
</style>
