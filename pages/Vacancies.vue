<template>
  <section class="overflow-hidden">
    <kinesis-container>
      <div class="container">
        <page-title
          title="Отправка резюме..."
          img="pageImg3"
        />
      </div>
    </kinesis-container>
  </section>
</template>

<script>
import { KinesisContainer, KinesisElement} from 'vue-kinesis'
import PageTitle from "@/components/pageTitle";
export default {
  name: "Vacancies",
  components: {
    PageTitle,
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement
  }
}
</script>

<style scoped>

</style>
