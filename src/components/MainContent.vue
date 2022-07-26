<template>
     <main>
      <div class="container deck">
      
            <BaseCard  />
          
        
      </div>
    </main>
</template>

<script>
import BaseCard from './BaseCard.vue'
export default {
name:"MainContent",
components: {BaseCard},
}
</script>

<style lang="scss" scoped>
/*main*/
main{
  background-color: #1E2D3B;
  height: calc(100vh - 50px);

  .deck{
    display: flex;
    flex-wrap: wrap;

  }
}
</style>