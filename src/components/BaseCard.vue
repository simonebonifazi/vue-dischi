<template>
    
  <div class="card">

    <figure>
      <img :src="card.poster">
          <figcaption>
            <h3 v-text="card.title"></h3>
             <h6 v-text="card.author"></h6>
             <h6 v-text="card.year"> </h6>
          </figcaption>
        </figure>
    
            </div>
</template>

<script>

export default {
    name:"BaseCard",
    props:{
        card: Object,
    },
    
}
</script>

<style lang="scss" scoped>
    .card{
   flex-basis: calc(20% - 30px);
   margin: 0 15px 15px 15px;    
   
   padding:15px;

    height: 300px;
    
    background-color: #2E3A46;

    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
     
    figure{
     margin: 8px 0;
        img{
          max-width:100%;
        }
      }
        h3,h6{
          color: #717778;
          font-size: 16px;
        }
        h3{
          margin: 20\px 0;

          color:#fff;
          text-transform: uppercase;
}
    }
</style>