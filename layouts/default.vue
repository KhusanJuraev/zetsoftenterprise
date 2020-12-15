<template>
  <kinesis-container>
    <Navbar
      v-if="$route.fullPath !== '/contacts'"
      class="position-fixed w-100 top"/>
    <Nuxt />
    <up-arrow v-if="$route.fullPath !== '/contacts'"/>
    <Footer v-if="$route.fullPath !== '/contacts'"/>

  </kinesis-container>
</template>

<script>
import Navbar from "@/components/Navbar";
import { KinesisContainer, KinesisElement} from 'vue-kinesis'
import Footer from "@/components/Footer";
import UpArrow from "@/components/upArrow";
export default {
  components: {
    UpArrow,
    Footer,
    Navbar,
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement
  },
  mounted: function () {
    console.log(this.$route.fullPath);
  }
}
</script>

<style>

input, textarea {
  background: #F9F9F9!important;
  border: 1px solid #E6E6E6!important;
  border-radius: 5px!important;
  padding: 12px 20px!important;
  min-width: 390px!important;
}
* {
  font-family: 'Montserrat', sans-serif;
  transition: .2s ease-in-out;
  scroll-behavior: smooth;
  perspective: none!important;
}
body {
  background: #FCFCFC;
}
section {
  margin-top: 100px;
}
@media (max-width: 993px) {
  section {
    margin-top: 50px;
  }
}
.top {
  top: 0;
}
.custom-control-inline {
  margin-bottom: 10px!important;
}
@media (min-width: 1200px) {
  .container, .container-sm, .container-md, .container-lg, .container-xl {
    max-width: 1540px;
  }
}
@media (max-width: 768px) {
  input, textarea {
    min-width: 100%!important;
  }
}
</style>
