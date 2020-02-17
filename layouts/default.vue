<template>
  <main class="wrapper">
    <div class="serf"/>
    <section class="content">
      <div class="nuxt-wrap">
        <Navbar/>
        <nuxt/>
        <Cards/>
      </div>
    </section>
  </main>
</template>
<script>
  import Navbar from "../components/Navbar";
  import Cards from "../components/cards";

  export default {
    components: {
      Navbar,
      Cards
    }
  }
</script>

