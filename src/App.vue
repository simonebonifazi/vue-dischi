<template>
  <div>
    <BaseHeader :genresList="genresList" />
    <MainContent :cards="cards"  />
   
  </div>
</template>

<script>
import axios from 'axios'
import BaseHeader from './components/BaseHeader.vue'
import MainContent from './components/MainContent.vue'
export default {
  name: 'SpotyDemo',
  components: {
    BaseHeader,
    MainContent,
  },
  data(){
    return{
        cards: [],
        genresList: []
    }
  },
  methods:{
    getAllCards(){
     axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((res)=>{
            this.cards= res.data.response;

          this.cards.forEach((card) => {
          if (!this.genresList.includes(card.genre)) this.genresList.push(card.genre);})
    })
    }
  },
      mounted(){
   this.getAllCards()
},
}
</script>

<style lang="scss">
/*generics*/
*{
  margin:0;
  padding:0;
  box-sizing: border-box;
}

body{
  font-family: 'Roboto', sans-serif;
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
