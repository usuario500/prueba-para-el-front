<template>
  <div>
    <div><MainMenu/></div>
    <br>
    <br>
    <br>
    <br>
    <div><TablasSolicitudes/></div>
    
  </div>
</template>

<script>
import MainMenu from './components/MainMenu.vue'
import TablasSolicitudes from './components/TablasSolicitudes.vue'

export default {
  
  name: 'App',
  components: {
    MainMenu,
    TablasSolicitudes
  }
}
</script>
