<template>
     <select name="search-for-genre" id="search-for-genre" @change="myChange" v-model="genreSelected" >
     <option value="">--Seleziona un Genere--</option>
        <option v-for="(genre,i) in genresList" :key="i" :value="genre" v-text="genre"></option>
       
    </select>
</template>

<script>
export default {
name: "GenreSelector",
props:{
    genresList: Array,
    
},
data(){
  return{
    genreSelected: "",
  }
},
methods: {
    myChange() {
      this.$emit("genre-choosed", this.genreSelected);
    },
  },
}
</script>

<style lang="scss" scoped>
 select{
    padding: 5px;
    border-radius: 5px;
  }

</style>