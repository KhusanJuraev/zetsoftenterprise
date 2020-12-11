<template>
  <kinesis-container>
    <Navbar class="position-fixed w-100 top"/>
    <Nuxt />

  </kinesis-container>
</template>

<script>
import Navbar from "@/components/Navbar";
import { KinesisContainer, KinesisElement} from 'vue-kinesis'
export default {
  components: {
    Navbar,
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement}
}
</script>

<style>
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

@media (min-width: 1200px) {
  .container, .container-sm, .container-md, .container-lg, .container-xl {
    max-width: 1540px;
  }
}
</style>
