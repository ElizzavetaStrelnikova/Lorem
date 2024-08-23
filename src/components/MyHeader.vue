<template>
  <div class="header_container container">
    <div class="menu-burger__header" @click="toggleMenu">
      <span></span>
    </div>
    <nav class="header__nav">
      <ul class="menu header__menu">
        <li><a href="" class="menu__item">Home</a></li>
      </ul>
    </nav>
    <h2 class="logo">Lorem</h2>
    <h2 class="title">Home</h2>
    <div class="contacts">
      <a href="mailto:elizaveta.strelnikova357@gmail.com"><img src="./../assets/svg/mail-svgrepo-com.svg" alt="mail"></a>
      <a href="https://t.me/elizavetastrelnikova"><img src="./../assets/svg/phone-svgrepo-com.svg" alt="phone"></a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'my-header',
  methods: {
    toggleMenu() {
      const header = document.querySelector('.menu-burger__header');
      header.classList.toggle('open-menu');
      const nav = document.querySelector('.header__nav');
      nav.classList.toggle('open-menu');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header_container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 15px 120px;
}
.header__nav {
  display: none;
}
.menu-burger__header {
  display: none;
}
.logo {
  color: #FFFFFF;
  padding: 8px 10px;
  background-color: black;
  font-size: 16px;
  animation: textflow 5s linear infinite;
}
.logo:hover {
  cursor: pointer;
  background: linear-gradient(90deg, darkgray, grey, black, darkgray, grey);
}
.title {
  color: #FF6E1F;
  font-size: 16px;
  font-family: 'Rawline-400', sans-serif;
  transition: 0.5s ease-in-out;
  cursor: pointer;
  display: block;
}
.title:hover {
  font-size: 20px;
}
.contacts {
  display: flex;
  flex-direction: row;
  gap: 20px;
}
.contacts img {
  cursor: pointer;
}
.container {
  margin: 0 auto;
}
@media (min-width: 320px) and (max-width: 1400px) {
.header_container {
  padding: 15px 20px;
}
  @media (min-width: 320px) and (max-width: 991px) {
    .title {
      display: none;
    }
    .menu-burger__header {
      position: relative;
      width: 40px;
      height: 35px;
      display: block;
      margin-left: 10px;
    }
    .menu-burger__header span, .menu-burger__header:after, .menu-burger__header:before{
      height: 3px;
      width: 100%;
      position: absolute;
      background: #515758;
      margin: 0 auto;
    }
    .menu-burger__header span{
      top: 21px;
    }
    .menu-burger__header:after, .menu-burger__header:before{
      content: '';
    }
    .menu-burger__header:after{
      bottom: 0px;
    }
    .menu-burger__header:before{
      top: 8px;
    }
    .header__nav {
      display: block;
      position: absolute;
      top: 55px;
      background: #FF6E1F;
      width: 20%;
      box-shadow: 0 4px 2px -2px rgba(36, 36, 36, 0.17);
      left: -100%;
      transition: all 0.4s ease;
    }
    .header__nav.open-menu {
      left: 0;
    }
    .menu-burger__header.open-menu span {
      opacity:0;
      transition: 0.5s;
    }
    .menu-burger__header.open-menu:before {
      transform: rotate(38deg);
      top: 16px;
      transition: 0.4s;
    }
    .menu-burger__header.open-menu:after {
      transform: rotate(-38deg);
      bottom: 16px;
      transition: 0.4s;
    }
    .header__menu {
      display: block;
      overflow: auto;
    }
    .header__menu li {
      margin: 40px 0px 40px 0px;
      font-size: 20px;
      list-style-type: none;
    }
    .menu__item {
      text-decoration: none;
      color: #FF6E1F;
    }
  }
}

</style>
