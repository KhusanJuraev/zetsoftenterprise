<template>
  <div class="page-title">

    <h2 class="position-relative text-center">
      {{ title }}
      <span>{{ title }}</span>
    </h2>

    <div class="page-img position-relative d-flex justify-content-center">
        <img :src="require(`@/assets/img/${img}.png`)" alt="img">
    </div>
  </div>
</template>

<script>
import { KinesisContainer, KinesisElement} from 'vue-kinesis'
export default {
  name: "pageTitle",
  props: ["title", "img"],
  components: {
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement
  }
}
</script>

<style scoped>
.page-title {
  margin: 25px 0 100px;
}
.page-title h2 {
  margin-bottom: 100px;
  font-weight: 900;
  font-size: 72px;
  color: #0047FF;
}
.page-title span {
  position: absolute;
  width: 100%;
  left: 0;
  font-size: 120px;
  opacity: .1;
  top: 0;
}
.page-title img {
  width: 90%;
  border-radius: 44px;
  position: relative;
}
.page-img:before {
  content: "";
  position: absolute;
  width: 90%;
  height: 100%;
  border-radius: 44px;
  transform: translate(4%, 8%);
  background: #0055f345;
}
</style>
