<template>
  <div class="page page-index">
    <div class="page-index--titlewrap">
      <div class="title">
        <h1>
          <span>Surf</span>
          <span>lessions</span>
        </h1>
        <p class="adv">Catch your first wave now</p>
      </div>
      <div class="info">
        <p>Now in bali</p>
        <p>January 9-22</p>
      </div>
    </div>
    <div>
      <div class="page-index--oval">
        <div>
          <img
            src="/man.svg"
            alt="photo"
          >
        </div>
        <div class="text">
          <p>Juli Star, 26 y.o</p>
          <p>“it was the best 3 hours of my life! So many emotions and my first wave”</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    components: {}
  }
</script>
<style scoped lang="scss">
  .page-index {
    display: flex;
    flex-direction: column;

    &--titlewrap {
      display: flex;

      .title {
        p {
          font-family: Qwigley;
          font-style: normal;
          font-weight: normal;
          font-size: 2vw;
          line-height: 113.5%;
          text-transform: capitalize;
          color: #30545C;
        }
      }

      .info {
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        margin: 0 0 2vw 7.4vw;

        p {
          font-family: 'Poppins';
          font-style: normal;
          font-weight: 900;
          font-size: 1.5vw;
          line-height: 113.5%;
          /* or 27px */
          text-transform: capitalize;
          color: #366E7A;
          border-left: 0.5vw solid white;
          padding-left: 1.818vw;

          &:last-child {
            font-weight: 300;
          }
        }
      }
    }

    &--oval {
      width: 22.5vw;
      height: 7.9vw;
      background: rgba(42, 74, 104, 0.51);
      backdrop-filter: blur(20px);
      border-radius: 6.25vw;
      display: flex;
      align-items: center;
      margin-top: 4.5vh;
      padding: 1.6vh 2vw;

      div {
        &:first-child {
          width: 5.625vw;
          height: 5.625vw;
          img {
            width: 100%;
            height: 100%;
            display: block;
          }
        }
      }
      .text{
        padding-left:1.25vw;
        width: 11.63vw;
        p{
          font-family: 'Poppins', sans-serif;
          font-style: normal;
          font-weight: 500;
          font-size: 0.75vw;
          line-height: 113.5%;
          text-transform: capitalize;
          color: #9BC9D3;
          &:first-child{
            font-style: normal;
            font-weight: bold;
            color: #EBF8F5;
            margin-bottom: 0.4vh;
          }
        }
      }
    }
  }
</style>
