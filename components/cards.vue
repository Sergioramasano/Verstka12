<template>
  <section>
    <div class="card">
      <button>
        <span>booking closed</span>
      </button>
      <div>
        <p>Bali</p>
        <p>January, 22</p>
      </div>
    </div>
    <div class="card">
      <button>
        <span>booking closed</span>
      </button>
      <div>
        <p>Bali</p>
        <p>January, 22</p>
      </div>
    </div>
    <div class="card">
      <button>
        <span>booking closed</span>
      </button>
      <div>
        <p>Bali</p>
        <p>January, 22</p>
      </div>
    </div>

  </section>
</template>

<script>
  export default {
    name: "Cards"
  }
</script>

<style scoped lang="scss">
  section{
    position: absolute;
    width: 100%;
    display: flex;
    justify-content: space-around;
    padding-left: 4.9vw;
    bottom: -10vh;
    @media screen and (max-width: 900px){
      bottom: -150px;
      flex-wrap: wrap;
      position: relative;
    }
    @media screen and (min-width:767px) and (max-width: 900px){
      bottom: -250px;
    }
    .card{
      width: 20.5vw;
      height: 19.17vh;
      padding:1.8vw 1vw 2.6vw;
      background-size: 100% 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      color: white;
      @media screen and (max-width: 900px){
        width: 250px;
        height: 150px;
        margin-top: 20px;
        margin-bottom: 20px;
      }
      &:first-child{
        background: url("/rect.svg") no-repeat;
      }
      &:nth-child(2){
        background: url("/rect1.svg") no-repeat;
      }
      &:last-child{
        background: url("/rect2.svg") no-repeat;
      }
      button{
        &:first-child{
          background: rgba(255, 255, 255, 0.74);
          backdrop-filter: blur(20px);
          border-radius: 50px;
          width: 8.4vw;
          height: 2.2vw;
          display: flex;
          justify-content: center;
          align-items: center;
          outline: none;
          border: none;
          @media screen and (max-width: 900px){
            width: 80%;
            height: auto;
            padding:10px 5px;
          }
        }
      }
    }
  }
</style>
