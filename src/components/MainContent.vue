<template>
     <main>
      <div class="container deck">
        <div class="card">
          <figure>
            <img src="https://img.discogs.com/vknPDdrqRbT92pNRX0W4I5N91jg=/fit-in/300x300/filters:strip_icc():format(jpeg):mode_rgb():quality(40)/discogs-images/R-1246953-1448927086-6590.jpeg.jpg" alt="bon jovi">
          </figure>
          <figcaption>
            <h3>titolo</h3>
            <h6>author</h6>
            <h6>year</h6>
          </figcaption>
        </div>
      </div>
    </main>
</template>

<script>
export default {
name:"MainContent",
}
</script>

<style lang="scss" scoped>
/*main*/
main{
  background-color: #1E2D3B;
  height: calc(100vh - 50px);
  overflow:hidden;
  .deck{
    display: flex;
    flex-wrap: wrap;
    .card{
      flex-basis: 20%;
      padding: 15px;

      height:225px;

      display:flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      
      figure{
        height: 60%;

        margin: 8px 0;

      }
          h3,h6{
            margin: 5px 0;
            color: #717778;
          }
    }
  }
}
</style>