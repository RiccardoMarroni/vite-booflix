<template>
  <HeaderComponent />
  <MainComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';

import axios from 'axios';
import { store } from './data/store';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent
  },
  data() {
    return{
      store,
    }
  },
  methods: {
    getApi(){
      axios.get(store.apiUrl)
      .then(result => {
        console.log(result.data)
      })
    }
  },
  mounted(){

  },
  computed(){

  },
}
</script>

<style lang="scss">

</style>

<!-- api
bf23213818e51de206214cfbb2cb2c83

eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJiZjIzMjEzODE4ZTUxZGUyMDYyMTRjZmJiMmNiMmM4MyIsInN1YiI6IjY2MWY4MTFjMjBhZjc3MDE3ZDNmMzRjNCIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.9tWQKIYCF5Pw61-cUic7CEEDzaSJg5oKIDXYemzaLrY -->