<template>
     <select name="search-for-genre" id="search-for-genre" >
        <!-- <option value="default">Seleziona genere</option>
        <option value="jazz">jazz</option>
        <option value="metal">metal</option>
        <option value="rock">rock</option>
        <option value="pop">pop</option> -->
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