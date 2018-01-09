<template>
  <div class="header">
      {{title}}
  </div>
</template>
<script>
    export default{
        name:'hello',
       data(){
           return{
               title:"首页"
           }
       }
    }
</script>
<style lang='scss'>
  .header{
      height: 40px;
      position: relative;
      top: 0;
      left: 0;
      background-color: #333;
      width: 100%;
  }
</style>

