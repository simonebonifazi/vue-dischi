<template>
     <select name="search-for-genre" id="search-for-genre" v-model="selectChoosed" >
        <option v-for="(genre,i) in genresList" :key="i" :value="genre" v-text="genre"></option>
       
    </select>
</template>

<script>
export default {
name: "GenreSelector",
props:{
    genresList: Array
},
data(){
  return{
    selectChoosed: "",
  }
}
}
</script>

<style lang="scss" scoped>
 select{
    padding: 5px;
    border-radius: 5px;
  }

</style>