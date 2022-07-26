<template>
  <div>
    <BaseHeader />
    <MainContent />
   
  </div>
</template>

<script>
import BaseHeader from './components/BaseHeader.vue'
import MainContent from './components/MainContent.vue'
export default {
  name: 'SpotyDemo',
  components: {
    BaseHeader,
    MainContent,
  }
}
</script>

<style lang="scss">
/*generics*/
*{
  margin:0;
  padding:0;
  box-sizing: border-box;
}
.container{
  width:976px;
  margin: 0 auto;
}

a{
  text-decoration: none;
  color:inherit;
}
ul{
  list-style-type: none;
}
img{
 width: auto;
 max-height: 100%;

 display: block;
}




</style>
