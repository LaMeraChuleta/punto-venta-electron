<template>
  <div id="app">
    <NavBarQuick></NavBarQuick>
    <router-view></router-view>    
  </div>
</template>

<script>
import NavBarQuick from './components/layout/NavBarQuick.vue'
export default {
  name: 'App',
  components: {    
    NavBarQuick
  }
}
</script>


