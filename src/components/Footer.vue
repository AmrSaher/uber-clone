<template>
    <footer class="
      w-full z-50 flex
      justify-around p-1
      mb-2 border-t-2
      border-t-gray-200
    ">
      <div class="grid place-items-center">
        <HomeIcon :size="30" fillColor="#1f1e1e" />
        <div class="w-full mt-1 text-xs text-center text-gray-800 font-semibold">
          Home
        </div>
      </div>
      <div class="grid place-items-center">
        <MapMarkerIcon :size="30" fillColor="#b3b1b1" />
        <div class="w-full mt-1 text-xs text-center text-gray-400 font-semibold">
          Destination
        </div>
      </div>
    </footer>
</template>

<script setup>
import HomeIcon from 'vue-material-design-icons/Home.vue'
import MapMarkerIcon from 'vue-material-design-icons/MapMarker.vue'
</script>