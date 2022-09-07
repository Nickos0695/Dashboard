<template>
  <div class="m-6 block p-6 max-w-sm bg-white rounded-lg border border-gray-200 shadow-md hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <h1 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Chuck Norris Fact</h1>
    <p class="font-normal text-gray-700 dark:text-gray-400">{{chuck.value}}</p>
  </div>
</template>

<script>
import axios from 'axios'

export default{
name:'ChuckNorris',
  data() {
    return {
      chuck: []
    }
  },
  mounted () {
    axios
      .get('https://api.chucknorris.io/jokes/random')
      .then(response => (this.chuck = response.data))
  },
}
</script>