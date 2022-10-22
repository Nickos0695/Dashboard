<template>
    <div class="m-6 block p-6 max-w-sm bg-white rounded-lg border border-gray-200 shadow-md hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
      <h1 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Zippopotame</h1>
      <p class="font-normal text-gray-700 dark:text-gray-400">{{zipo}}</p>
    </div>
  </template>
  
  <script>
  import axios from 'axios'
  
  export default{
  name:'Zipopotam',
    data() {
      return {
        zipo: []
      }
    },
    mounted () {
      axios
        .get('https://api.zippopotam.us/FR/06000')
        .then(response => (this.zipo = response.data))
    },
  }
  </script>