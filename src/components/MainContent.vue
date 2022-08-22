<template>
  <main>
    <div class="container deck">

      <BaseCard v-for="(card, i) in filteredCards" :key="i" :card="card" />

    </div>
  </main>
</template>

<script>
import BaseCard from './BaseCard.vue';
export default {
name:"MainContent",
components: {BaseCard},
data(){
        return{
        }
    },
    props:{
      cards: Array,
      selectedGenre: String,
    },
    computed: {
      filteredCards(){
        if(!this.selectedGenre) return this.cards;
        return this.cards.filter((card)=>{
          if(card.genre === this.selectedGenre) return true;
          else return false;
        })
      }
    },

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