<script>
import {store} from './data/store'
export default {
  name: 'AppRicerca',
  data(){
    return{
      store
    }
  },
  methods:{
    reset(){
      store.memberSearch = '',
      store.statusSearch = '',
      this.$emit('startSearch');
    }
  }
}
</script>

<template>
  <div class="container mb-5 d-flex justify-content-center">
    <div class="row">
      <div class="col-auto">
        <input v-model="store.memberSearch" type="text" class="form-control" placeholder="Search Character">
      </div>
      <div class="col-auto">
        <select v-model="store.statusSearch" class="form-select">
          <option value="" selected>Select Category</option>
          <option value="breaking bad">Breaking Bad</option>
          <option value="better call saul">Better Call Saul</option>
</select>
      </div>
      <div class="col-auto">
        <button @click="$emit('startSearch')" type="button" class="btn btn-outline-light">Search</button>
      </div>
      <div class="col-auto">
        <button @click="reset()" type="button" class="btn btn-outline-light">Reset</button>
      </div>
    </div>
  </div>
</template> 

<style lang="scss" scoped>

</style>