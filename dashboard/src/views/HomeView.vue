<template>
<Header/>
<div class="grid-cols-3	">
  <ChuckNorris/>
  <Maps/>
  <Zippopotam/>
</div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue';
import ChuckNorris from '@/components/ChuckNorris.vue';
import Maps from '../components/Maps.vue';
import Zippopotam from '@/components/Zippopotam.vue';

export default {
  name: 'HomeView',
  components: {
    Header,
    ChuckNorris,
    Maps,
    Zippopotam
}
}
</script>
