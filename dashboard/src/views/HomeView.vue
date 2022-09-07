<template>
<Header/>
<div class="grid-cols-3	">
  <ChuckNorris/>
</div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue';
import ChuckNorris from '@/components/ChuckNorris.vue';

export default {
  name: 'HomeView',
  components: {
    Header,
    ChuckNorris,
  }
}
</script>
