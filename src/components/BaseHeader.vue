<template>
  <header>
    <figure>
      <img src="https://th.bing.com/th/id/R.57dd160d1e8f82b1113ca3f73393621c?rik=EHp%2bG6a6uyaHaA&pid=ImgRaw&r=0"
        alt="logo">
    </figure>

    <GenreSelector :genresList="genresList" @genre-choosed="getGenreValue" />

  </header>
</template>

<script>
 import GenreSelector from './GenreSelector.vue'
export default {
name: "BaseHeader",
 components: {GenreSelector,},
props: {
  genresList: Array
},
methods:{
  getGenreValue(genre){
    this.$emit("genre-change", genre);
  
  }
}

}
</script>

<style lang="scss" scoped>
header{
  padding: 15px;
  height: 75px;
  background-color: #2E3A46;

  display:flex;
  justify-content: space-between;
  align-items: center;

  figure{
    height: 100%;
  }
  
}
</style>