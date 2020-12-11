<template>
    <img :src="require(`@/assets/img/client${count}.png`)" alt="" class="client">
</template>

<script>
export default {
  name: "client",
  props: ["count"],
}
</script>

<style scoped>
.client {
  margin: 0 40px 40px;
  opacity: .7;
}
.client:hover {
  opacity: 1;
}
</style>
