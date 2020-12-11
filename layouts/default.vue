<template>
  <kinesis-container>
    <Navbar class="position-fixed w-100 top"/>
    <Nuxt />
    <Footer />
  </kinesis-container>
</template>

<script>
import Navbar from "@/components/Navbar";
import { KinesisContainer, KinesisElement} from 'vue-kinesis'
import Footer from "@/components/Footer";
export default {
  components: {
    Footer,
    Navbar,
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement}
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
</style>
