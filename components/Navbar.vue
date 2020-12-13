<template>
  <header>
    <b-navbar class="bg-blue" toggleable="lg" type="dark">
      <Logo />

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto mr-4">
          <nuxt-link class="nav-link" exact-active-class="active" to="/">ГЛАВНАЯ</nuxt-link>
          <nuxt-link class="nav-link" active-class="active" to="/about">О НАС</nuxt-link>
          <nuxt-link class="nav-link" active-class="active" to="/services">УСЛУГИ</nuxt-link>
          <nuxt-link class="nav-link" active-class="active" to="/vacancies">ВАКАНСИИ</nuxt-link>
          <nuxt-link class="nav-link" active-class="active" to="/contacts">КОНТАКТЫ</nuxt-link>
        </b-navbar-nav>

        <b-navbar-nav>
          <b-button pill size="sm" class="my-2 my-sm-0 bg-white border-0 p-2 px-3 my-md-1" type="submit">
            <BIconTelephoneFill class="text-primary"/>
            <span class="text-primary font-weight-bold">+998(71) 200 74 77</span>
          </b-button>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </header>
</template>

<script>
import {BIcon, BIconTelephoneFill} from 'bootstrap-vue'
import Logo from "@/components/Logo";
export default {
  name: "Navbar",
  components: {
    Logo,
    BIcon,
    BIconTelephoneFill,
  }
}
</script>

<style scoped>
.nav-link {
  position: relative;
  font-size: 14px;
  border-bottom: 2px solid transparent;
  margin: 0 10px;
}
.nav-link:before {
  content: '';
  position: absolute;
  bottom: -3px;
  left: 0;
  width: 100%;
  height: 2px;
  background: #fff;
  transition: .3s ease-in-out;
  opacity: 0;
}
.nav-link:hover::before {
  width: 100% !important;
  opacity: 1;
}
.active {
  border-bottom: 2px solid #fff;
}
.bg-blue {
  background-image: url("../assets/img/bg.png");
  background-position: bottom;
  background-origin: border-box;
  background-attachment: fixed;
  background-size: cover;
  background-repeat: no-repeat;
}
header {
  z-index: 1000;
}
</style>
