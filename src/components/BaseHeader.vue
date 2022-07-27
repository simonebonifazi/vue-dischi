<template>
  <header> 
      <figure>
        <img src="https://th.bing.com/th/id/R.57dd160d1e8f82b1113ca3f73393621c?rik=EHp%2bG6a6uyaHaA&pid=ImgRaw&r=0" alt="logo">
      </figure>

  
    <select name="search-for-genre" id="genre-searcher" >
        <option value="default">Seleziona genere</option>
        <option value="jazz">jazz</option>
        <option value="metal">metal</option>
        <option value="rock">rock</option>
        <option value="pop">pop</option>
    </select>
  </header>
</template>

<script>
export default {
name: "BaseHeader"
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
  select{
    padding: 5px;
    border-radius: 5px;
  }

}
</style>