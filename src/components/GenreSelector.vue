<template>
     <select name="search-for-genre" id="search-for-genre" >
        <option value="default">Seleziona genere</option>
       
    </select>
</template>

<script>
export default {
name: "GenreSelector",
props:{
    option: Array,
}
}
</script>

<style lang="scss" scoped>
 select{
    padding: 5px;
    border-radius: 5px;
  }

</style>