<template>
  <div>
    <header> 
      <figure>
        <img src="https://th.bing.com/th/id/R.57dd160d1e8f82b1113ca3f73393621c?rik=EHp%2bG6a6uyaHaA&pid=ImgRaw&r=0" alt="logo">
      </figure>
    </header>
    <main>
      <div class="discs">
        <div class="single-disc"></div>
      </div>
    </main>
  </div>
</template>

<script>
import BaseHeader from './components'
export default {
  name: 'App',
  components: {
    BaseHeader,
  }
}
</script>

<style lang="scss">
/*generics*/
*{
  margin:0;
  padding:0;
  box-sizing: border-box;
}
header{
  height: 100px;
  background-color: #2E3A46;
  figure{
    height: 100%;
    display:flex;
    justify-content: flex-start;
    align-items: center;
  }
  img{
    width: auto;
    max-height: 100%;
  }
}

</style>
