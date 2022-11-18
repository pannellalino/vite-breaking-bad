<script>

import {store} from './data/store'

  export default {
    name: 'AppCard',
    data(){
      return{
        store
      }
    }
  }
</script>


<template>
  <div class="container d-flex flex-wrap p-4">
    <div v-for="member in store.memberList" :key="member.char_id"
    class="card p-4 border-0 mb-4">
    <img :src="member.img" :alt="member.name">
    <h5 class="text-light text-center m-2">{{member.name}}</h5>
    <span class="text-center m-2">{{member.category}}</span>
    <span class="text-center m-2">{{member.status}}</span>
  </div>
  </div>
</template>


<style lang="scss" scoped>

@use '../styles/partials/vars' as *;
.container.d-flex{
  background-color: white;
  .card{
    width: calc(100% / 5 - 5px);
    background-color: $primary-color;
    margin-right: 5px;
    border-radius: 0;
    span{
      color: gray;
      font-size: .8rem;
    }
  }
}

</style>