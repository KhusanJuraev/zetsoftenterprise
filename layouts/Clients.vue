<template>
  <section>
    <div class="container">
      <Title
        title="ВЫБРАННЫЕ КЛИЕНТЫ"
        text="Вот некоторые бренды, с которыми мы имели честь работать"
      />
      <div class="clients d-flex flex-wrap justify-content-between align-items-center">
        <Client
          v-for="count in 8"
          v-bind:count="count"
        />
      </div>
    </div>
  </section>
</template>

<script>
import Title from "@/components/Title";
import Client from "@/components/Client";
export default {
  name: "Clients",
  components: {Client, Title},
  data() {
    return {

    }
  }
}
</script>

<style scoped>

</style>
