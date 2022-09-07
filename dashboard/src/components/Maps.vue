<template>
<div class="m-6 block p-6 max-w-sm bg-white rounded-lg border border-gray-200 shadow-md hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <div>
      <h1 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{ msg }}</h1>
  
      <div id="myMap"></div>
    </div>
</div>
  </template>
  
  <script>
  export default {
    name: 'hello',
    data () {
      return {
        msg: 'Google Maps'
      }},
    mounted: function() {
          console.log("map: ", google.maps)
              this.map = new google.maps.Map(document.getElementById('myMap'), {
              center: {lat:61.180059, lng: -149.822075},
              scrollwheel: false,
              zoom: 4
              })
    }
  
  }
  </script>
  <style scoped>
      #myMap {
      height:300px;
      width: 100%;
     }
  </style>