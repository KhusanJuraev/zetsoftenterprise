<template>
  <kinesis-container>
    <div class="offer-card d-flex justify-content-center align-items-center">
      <kinesis-element type="depth">
        <div class="offer-card-block d-flex flex-column align-items-center justify-content-center">
          <kinesis-element>
            <img :src="require(`@/assets/img/${svg}.png`)" alt="">
          </kinesis-element>
          <p>{{ text }}</p>
          <kinesis-element>
            <nuxt-link to="/about">ПОДРОБНО</nuxt-link>
          </kinesis-element>
        </div>
      </kinesis-element>
    </div>
  </kinesis-container>
</template>

<script>
import { KinesisContainer, KinesisElement} from 'vue-kinesis'

export default {
  name: "OfferCards",
  props: ["svg", "text"],
  components: {
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement,
  }
}
</script>

<style scoped>
.offer-card {
  max-width: 360px;
  height: 408px;
  background: #FFFFFF;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  border-radius: 44px;
  padding: 30px 0;
}
.offer-card-block {
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  border-radius: 44px;
  height: 100%;
  padding: 20px;
  text-align: center;
}
.offer-card:hover {
  box-shadow: 0 12px 50px rgba(0, 0, 0, 0.1);
}
.offer-card:hover .offer-card-block {
  box-shadow: 0 12px 50px rgba(0, 0, 0, 0.1);
}
.offer-card-block img {
  width: 120px;
}
.offer-card-block p {
  margin: 30px 0;
  font-size: 18px;
  color: #1A2863;
}
.offer-card-block a {
  color: #061552;
  font-weight: 500;
}
</style>
