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
        <li>
          <nuxt-link
            to="/about"
          >About
          </nuxt-link>
        </li>
        <li>
          <nuxt-link
            to="/teachers"
          >Teachers
          </nuxt-link>

        </li>
        <li>
          <nuxt-link
            to="/price"
          >Price
          </nuxt-link>

        </li>
        <li>
          <nuxt-link
            to="/shedule"
          >Shedule
          </nuxt-link>

        </li>
        <li>
          <nuxt-link
            to="/contacts"
          >Contacts
          </nuxt-link>

        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
  export default {
    name: "Navbar"
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
          a {
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
    }
  }

</style>
