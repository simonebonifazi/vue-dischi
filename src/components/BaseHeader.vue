<template>
  <header> 
      <figure>
        <img src="https://th.bing.com/th/id/R.57dd160d1e8f82b1113ca3f73393621c?rik=EHp%2bG6a6uyaHaA&pid=ImgRaw&r=0" alt="logo">
      </figure>
    </header>
</template>

<script>
export default {
name: "BaseHeader"
}
</script>

<style lang="scss" scoped>
header{
  height: 100px;
  background-color: #2E3A46;
  figure{
    height: 100%;
    display:flex;
    justify-content: flex-start;
    align-items: center;
  }

}
</style>