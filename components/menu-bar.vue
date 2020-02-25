<template>
  <div
    class="hamburger-menu"
  >
    <input
      id="menu__toggle"
      ref="closer"
      type="checkbox"
    >
    <label
      class="menu__btn"
      for="menu__toggle">
      <span/>
    </label>
    <ul class="menu__box">
      <li
        v-for="item in items"
        :key="item"
        @click="clickCloser"
      >
        <nuxt-link
          :to="`/${item.toLowerCase()}`"
          class="menu__item"
        >{{ item }}
        </nuxt-link>
      </li>
    </ul>
    <div
      id="layer"
      @click="clickCloser"
    />
  </div>
</template>

<script>
    export default {
        name: "MenuBar",
        data:()=>({
            items:[
                'About',
                'Teachers',
                'Price',
                'Shedule',
                'Contacts'
            ]
        }),
        methods:{
            clickCloser(){
                this.$refs.closer.click()
            }
        }
    }
</script>

<style scoped lang="scss">
  #layer{
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    background-color: black;
    opacity: 0.6;
    z-index: 200;
    display: none;
  }
  /* скрываем чекбокс */
  #menu__toggle {
    opacity: 0;
  }

  /* стилизуем кнопку */
  .menu__btn {
    display: flex; /* используем flex для центрирования содержимого */
    align-items: center; /* центрируем содержимое кнопки */
    position: fixed;
    top: 10px;
    right: 20px;
    width: 26px;
    height: 26px;
    cursor: pointer;
    z-index: 1000;
  }

  /* добавляем "гамбургер" */
  .menu__btn > span,
  .menu__btn > span::before,
  .menu__btn > span::after {
    display: block;
    position: absolute;
    width: 100%;
    height: 2px;
    background-color: #ffffff;
  }

  .menu__btn > span::before {
    content: '';
    top: -8px;
  }

  .menu__btn > span::after {
    content: '';
    top: 8px;
  }

  /* контейнер меню */
  .menu__box {
    display: block;
    position: fixed;
    top: 0;
    left: -100%;
    width:70%;
    height: 100%;
    margin: 0;
    padding: 80px 0;
    list-style: none;
    text-align: center;
    background-color: #366e7a;
    box-shadow: 1px 0px 6px rgba(0, 0, 0, .2);
    z-index: 999;
    @media screen and (max-width: 400px){
     width: 100%;
    }
  }

  /* элементы меню */
  .menu__item {
    display: block;
    padding: 12px 24px;
    color: #CFD8DC;
    font-family: 'Qwigley', cursive;
    font-size: 40px;
    font-weight: 600;
    text-decoration: none;
  }

  .menu__item:hover {
    background-color:#333;
    cursor: pointer;
    transition: 1s ease;
  }

  #menu__toggle:checked ~ .menu__btn > span {
    transform: rotate(45deg);
  }

  #menu__toggle:checked ~ .menu__btn > span::before {
    top: 0;
    transform: rotate(0);
  }

  #menu__toggle:checked ~ .menu__btn > span::after {
    top: 0;
    transform: rotate(90deg);
  }

  #menu__toggle:checked ~ .menu__box {
    visibility: visible;
    left: 0;
  }
  #menu__toggle:checked ~ #layer {
   display: block;
  }

  .menu__btn > span,
  .menu__btn > span::before,
  .menu__btn > span::after {
    transition-duration: .25s;
  }

  .menu__box {
    transition-duration: .25s;
  }

  .menu__item {
    transition-duration: .25s;
  }
</style>
