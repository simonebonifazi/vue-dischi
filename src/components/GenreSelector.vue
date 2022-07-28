<template>
     <select name="search-for-genre" id="search-for-genre" >
        <option value="default"> --Seleziona una voce--</option>
        <option v-for="(genre,i) in genresList" :key="i" :value="genre" v-text="genre"></option>
       
    </select>
</template>

<script>
export default {
name: "GenreSelector",
props:{
    genresList: Array
}
}
</script>

<style lang="scss" scoped>
 select{
    padding: 5px;
    border-radius: 5px;
  }

</style>