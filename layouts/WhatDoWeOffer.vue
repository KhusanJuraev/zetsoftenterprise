<template>
  <section>
    <div class="container">
      <Title title="ЧТО МЫ ПРЕДЛАГАЕМ?"/>
      <div class="offer-cards d-flex flex-wrap justify-content-around">
        <OfferCards
          v-for="offer of offers"
          v-bind:svg="offer.svg"
          v-bind:text="offer.text"
        />
      </div>
    </div>
  </section>
</template>

<script>
import Title from "@/components/Title";
import OfferCards from "@/components/OfferCard";
export default {
  name: "WhatDoWeOffer",
  components: {OfferCards, Title},
  data() {
    return {
      offers: [
        {
          svg: 'offer1',
          text: 'Качественные сайты любого уровня сложности по последним трендам'
        },
        {
          svg: 'offer2',
          text: 'Мобильные приложения отвечающие требованиям мировых стандартов'
        },
        {
          svg: 'offer3',
          text: 'Умные телеграм боты для упрощения и повышения эффективности бизнеса'
        },
        {
          svg: 'offer4',
          text: 'Креативный, индивидуальный адаптивный веб-дизайн сайта.'
        },
      ]
    }
  }
}
</script>

<style scoped>

</style>
