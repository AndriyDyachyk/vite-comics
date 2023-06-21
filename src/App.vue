<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
export default {
  data(){
    return{

    }
  },
  components:{
    AppHeader,
    AppMain,
    AppFooter
  },
  methods:{
  }
}
</script>
<template lang="">
  <div>
    <AppHeader />
    <AppMain />
    <AppFooter />
  </div>
</template>
<style lang="scss">
  @use './styles/general.scss' as *;
  @import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@200;300;400;500;600;700&display=swap');
</style>