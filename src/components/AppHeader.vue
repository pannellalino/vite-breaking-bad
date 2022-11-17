<script>
  export default {
    name: 'AppHeader'
  
  }
</script>


<template>
  <header>
    <div class="logo p-2 d-flex align-items-center">
      <img src="../assets/img/Breaking_Bad_logo.svg" alt="Logo">
      <h1 class="ms-4 mb-0">Breaking Bad Api</h1>
    </div>
  </header>
</template>


<style lang="scss" scoped>

header{
  background-color: white;
  img{
    height: 40px;
  }
  h1{
    font-weight: 800;
  }
}

</style>