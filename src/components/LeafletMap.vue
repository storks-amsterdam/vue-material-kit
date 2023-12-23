<template>
  <div style="height: 600px; width: w-80">
    <l-map
      ref="map"
      v-model:zoom="zoom"
      :center="[52.3676, 4.9041]"
      :use-global-leaflet="false"
    >
      <l-tile-layer
        url="https://tile.openstreetmap.org/{z}/{x}/{y}.png"
        layer-type="base"
        name="OpenStreetMap"
        attribution='&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
      ></l-tile-layer>
      <l-wms-tile-layer
        url="https://services.sentinel-hub.com/ogc/wms/4716c380-9626-4b71-a620-2f925fb00521"
        attribution='&copy; <a href="http://www.sentinel-hub.com/" target="_blank">Sentinel Hub</a>'
        layer-type="overlay"
        name="Sentinel NDVI"
        :max-zoom="16"
        :min-zoom="6"
        version="1.3.0"
        format="image/png"
        :transparent="true"
        layers="NDVI"
        preset="NDVI"
        urlProcessingApi="https://services.sentinel-hub.com/ogc/wms/1d4de4a3-2f50-493c-abd8-861dec3ae6b2"
        maxcc="20"
        time="2022-12-01/2023-06-12"
      ></l-wms-tile-layer>
      <l-control-layers />
    </l-map>
  </div>
</template>

<script>
import "leaflet/dist/leaflet.css";
import { LMap, LControlLayers, LTileLayer, LWmsTileLayer } from "@vue-leaflet/vue-leaflet";

export default {
  components: {
    LMap,
    LTileLayer,
    LWmsTileLayer,
    LControlLayers,
  },
  data() {
    return {
      zoom: 12,
    };
  }
};
</script>

<style></style>
