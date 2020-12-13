<template>
  <div class="feature d-flex flex-wrap justify-content-around align-items-center">
    <div class="feature-content">
      <h3 class="pb-3">{{ title }}</h3>
      <p>{{ text }}</p>
    </div>
    <div class="feature-illustration">
      <img :src="require(`@/assets/img/${svg}.png`)" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: "Feature",
  props: ["title", "text", "svg"]
}
</script>

<style scoped>
.feature {
  margin: 100px 0;
}
.feature-content {
  max-width: 650px;
}
.feature-content h3 {
  font-weight: bold;
  font-size: 28px;
  color: #061552;
}
.feature-content p {
  font-weight: normal;
  font-size: 18px;
  color: #1A2863;
}
.feature-illustration img {
  max-width: 600px;
}
</style>
