<template>
  <kinesis-container>
    <kinesis-element type="depth">
      <div class="card-services">
        <kinesis-element>
          <div class="card-header d-flex flex-column align-items-center">
            <kinesis-element>
              <img :src="require(`@/assets/img/svg${svg}.png`)" alt="svg" class="my-3">
            </kinesis-element>
            <span>{{ title }}</span>
          </div>
        </kinesis-element>
        <div class="card-description">
          <kinesis-element>
            <p>
              {{ description }}
            </p>
          </kinesis-element>
        </div>
      </div>
    </kinesis-element>
  </kinesis-container>
</template>

<script>
import { KinesisContainer, KinesisElement} from 'vue-kinesis'

export default {
  name: 'ServicesCard',
  props: ['svg','title','description'],
  components: {
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement,
  }
}
</script>

<style scoped>
.card-services {
  width: 360px;
  height: 390px;
  background: #FFFFFF;
  box-shadow: 0 3px 12px rgba(0, 0, 0, 0.1);
  border-radius: 45px;
  padding: 20px;
  margin-bottom: 20px;
}
.card-services:hover {
  box-shadow: 0 12px 50px rgba(0, 0, 0, 0.1);
}
.card-services:hover .card-header {
  box-shadow: 0 12px 50px rgba(0, 0, 0, 0.1);
}
.card-header {
  width: 100%;
  background: #FFFFFF;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  border-radius: 45px;
}
.card-header img {
  width: 100px;
}
.card-header span {
  font-weight: 600;
  font-size: 18px;
  text-align: center;
  color: #061552;
}
.card-description {
  padding: 20px 0;
}
.card-description p {
  font-weight: 400;
  font-size: 16px;
  text-align: center;
  color: #1A2863;
}
</style>
