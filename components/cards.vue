<template>
  <section>
    <div class="card">
      <div>
        <span>booking closed</span>
      </div>
      <div>
        <p>Bali</p>
        <p>January, 22</p>
      </div>
    </div>
    <div class="card">
      <div>
        <span>booking closed</span>
      </div>
      <div>
        <p>Bali</p>
        <p>January, 22</p>
      </div>
    </div>
    <div class="card">
      <div>
        <span>booking closed</span>
      </div>
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
    .card{
      width: 20.5vw;
      height: 19.17vh;
      padding:1.8vw 1vw 2.6vw;
      background-size: 100% 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      color: white;
      &:first-child{
        background: url("/rect.svg") no-repeat;
      }
      &:nth-child(2){
        background: url("/rect1.svg") no-repeat;
      }
      &:last-child{
        background: url("/rect2.svg") no-repeat;
      }
      div{
        &:first-child{
          background: rgba(255, 255, 255, 0.74);
          backdrop-filter: blur(20px);
          border-radius: 50px;
          width: 8.4vw;
          height: 2.2vw;
          display: flex;
          justify-content: center;
          align-items: center;
        }
      }
    }
  }
</style>
