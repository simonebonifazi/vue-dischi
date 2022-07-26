<template>
  <div>
    <BaseHeader />
    
    <main>
      <div class="discs">
        <div class="single-disc"></div>
      </div>
    </main>
  </div>
</template>

<script>
import BaseHeader from './components/BaseHeader.vue'
export default {
  name: 'App',
  components: {
    BaseHeader,
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
  width:1080px;
  margin: 0 auto;
}

a{
  text-decoration: none;
  color:inherit;
}
ul{
  list-style-type: none;
}

</style>
