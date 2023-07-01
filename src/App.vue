<template>
  <div class="container">
    <MainPage />
  </div>
</template>

<script>
import MainPage from './pages/MainPage.vue'

export default {
  components:{
    MainPage
  }
}
</script>

<style scoped lang="scss">
.container{
  display: flex;
  flex-direction: column;
  gap: 32px;
  
  width: 1400px;
  margin: 24px auto;
}
</style>
