<template>
     <main>
      <div class="container deck">
      
            <BaseCard v-for="(card, i) in cards" :key="i" :card="card" />
          
        
      </div>
    </main>
</template>

<script>
import axios from 'axios'
import BaseCard from './BaseCard.vue'
export default {
name:"MainContent",
components: {BaseCard},
data(){
        return{
            cards: []

        }
    },
    mounted(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((res)=>{
            this.cards= res.data.response
        
        })
    }
}
</script>

<style lang="scss" scoped>
/*main*/
main{
  background-color: #1E2D3B;
  height: calc(100% - 50px);

  width:100%;

  padding: 100px;
  .deck{
    display: flex;
    flex-wrap: wrap;
  
  }
}
</style>