<template>
     <main>

      <select name="search-for-genre" id="search-for-genre"  v-model="genreSelected">  
              <option v-for="(genre, i) in genres" :key="i" :value="genre" >
           {{ genre }}
            </option>
        <!-- <option v-for="(genre, i) in filteredByGenre" :key="i" :value="genre.value" ></option> -->
        <!-- <option value="Jazz">jazz</option>
        <option value="Metal">metal</option>
        <option value="Rock">rock</option>
        <option value="Pop">pop</option> -->
    </select>

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
            genreSelected:"",
            cards: [],
            genres: []
        }
    },
    mounted(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((res)=>{
            this.cards= res.data.response;

          this.cards.forEach((card) => {
          if (!this.genres.includes(card.genre)) this.genres.push(card.genre);})
    })
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