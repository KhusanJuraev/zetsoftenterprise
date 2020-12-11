<template>
  <div class="title">
    <h3>{{ title }}</h3>
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: "Title",
  props: ["title", "text"]
}
</script>

<style scoped>
.title {
  margin-bottom: 100px;
  text-align: center;
  width: 100%;
}
.title h3 {
  font-size: 36px;
  font-weight: 900;
  color: #061552;
}
.title p {
  font-size: 18px;
  width: 700px;
  margin: 0 auto;
  color: #1A2863;
}

@media (max-width: 768px) {
  .title h3 {
    font-size: 32px;
  }
  .title p {
    width: 100%;
  }
}
</style>
