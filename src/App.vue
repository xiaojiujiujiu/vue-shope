<template>
  <div id="app">
    <v-header></v-header>
    <router-view/>
  </div>
</template>

<script>
import Header from './components/header'; 
export default {
  name: 'app',
  components:{
    'v-header':Header
  }
}
</script>

<style>
 @import './../static/css/reset.css';
</style>
