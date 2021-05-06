<template>
  <div id="map">

  </div>
</template>

<script>
import Mapbox from "mapbox-gl";

export default {
  components: {
  },
  data() {
    return {
    };
  },
  mounted() {
    // We need to set mapbox-gl library here in order to use it in template
    this.mapbox = new Mapbox.Map({
        container: 'map',
        accessToken:
        "pk.eyJ1IjoibWlrZWhhbWlsdG9uMDAiLCJhIjoiNDVjS2puUSJ9.aLvWM5BnllUGJ0e6nwMSEg",
        style: 'mapbox://styles/mapbox/streets-v11',
        center: [16.3333300, 53.4577500],
        zoom: 11
    })
  },
};
</script>
<style>
#map {
    height: 100%;
    width: 100%;
}
</style>