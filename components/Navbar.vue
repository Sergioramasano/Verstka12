<template>
  <header>
    <nuxt-link
      to="/"
      exact
      no-prefetch
      class="logo"
    />
    <nav>
      <ul>
        <li
          v-for="item in items"
          :key="item">
          <nuxt-link
            :to="`/${item.toLowerCase()}`"
            class="menu__item"
          >{{ item }}
          </nuxt-link>
        </li>
      </ul>
    </nav>
    <menu-bar/>
  </header>
</template>

<script>
  import MenuBar from "./menu-bar";
  export default {
    name: "Navbar",
      components: {MenuBar},
      data:()=>({
          items:[
              'About',
              'Teachers',
              'Price',
              'Shedule',
              'Contacts'
          ]
      })
  }
</script>

<style scoped lang="scss">
  header {
    display: flex;
    justify-content: space-between;
    padding: 2.3vh 8vw 2.3vh 4.9vw;

    .logo {
      display: block;
      width: 6.19vw;
      height: 3vh;
      background: url("../static/logo.svg") no-repeat;
      background-size: contain;
      @media screen and (max-width: 900px){
        width: 100px;
        height: 50px;
      }
      &:hover{
        transition: 1s ease;
        transform: rotateZ(10deg);
      }
    }

    nav {
      width: 50%;
      display: flex;
      align-items: center;
      margin: auto;
      ul {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        li {
          display: block;
          cursor: pointer;
          display: block;
          .menu__item {
            display: block;
            text-decoration: none;
            font-family: Qwigley;
            font-style: normal;
            font-weight: normal;
            font-size: 2vw;
            text-transform: capitalize;
            font-family: 'Qwigley', cursive;
            &:hover{
              color: #000;
              transition: 1s ease;
            }
          }
        }
      }
      @media screen and (max-width: 900px){
       display: none;
      }
    }
  }
</style>
