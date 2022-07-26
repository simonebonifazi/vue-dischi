<template>
    <div >

        <figure class="card" v-for="card in cards" :key="card.title">
            <img :src="card.poster">
          <figcaption>
             <h3 v-text="card.title"></h3>
             <h6 v-text="card.author"></h6>
             <h6 v-text="card.genre"> </h6>
             <h6 v-text="card.year"> </h6>
          </figcaption>
        </figure>
    </div>
</template>

<script>
import axios from "axios"
export default {
    name:"BaseCard",
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
    .card{
      flex-basis: 20%;
      padding: 15px;

      height:225px;

      background-color: #2E3A46;
      margin: 50px 0;

      text-align: center;

      
      display:flex;
      flex-direction: column;
      align-items: center;
      
      
    
    figure{
        height: 60%;

        margin: 8px 0;

      }
          h3,h6{
            margin: 5px 0;
            color: #717778;
          }
    }
</style>