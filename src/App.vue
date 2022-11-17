<script>
import axios from 'axios';
import {store} from './components/data/store'

import AppHeader from './components/AppHeader.vue';
import AppCard from './components/AppCard.vue';

  export default {
    name: 'App',
    components:{
      AppHeader,
      AppCard
    },
    data(){
      return{
        store
      }
    },
    methods:{
      getApi(){
        axios.get(store.apiUrl)
        .then(result =>{
          store.memberList = result.data
          console.log(store.memberList);
        })
        .catch(error =>{
          console.log(error);
        })
      }
    },
    mounted(){
      this.getApi()
    }
  
  }
</script>


<template>
  <AppHeader />
  <main>
    <AppCard />
  </main>
</template>


<style lang="scss">
@use './styles/generals.scss';
@use './styles/partials/vars' as *;

main{
  background-color: $primary-color;
  min-height: 100vh;
  padding: 50px;
}

</style>