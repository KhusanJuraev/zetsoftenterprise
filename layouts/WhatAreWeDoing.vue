<template>
  <section>
    <div class="container">
      <Title v-bind:title="title" v-bind:text="text"/>
      <div class="services-cards d-flex justify-content-around flex-wrap align-items-center">
        <ServicesCard
          v-for="service of services"
          v-bind:svg="service.svg"
          v-bind:title="service.title"
          v-bind:description="service.description"
        />
      </div>
    </div>
  </section>
</template>

<script>
import Title from "@/components/Title";
import ServicesCard from "@/components/ServicesCard";

export default {
  name: "WhatAreWeDoing",
  components: {ServicesCard, Title},

  data() {
    return {
      title: 'ЧТО МЫ ДЕЛАЕМ?',
      text: 'Наши услуги разработаны так, чтобы ваш бизнес рос и выделялся',
      services: [
        {
          svg: '1',
          title: 'Landing-page',
          description: 'Лендинг формируется таким образом, чтобы коротко и доходчиво изложить суть предложения, вызвать заинтересованность, убедить клиента в том, что это то чего он желает.'
        },
        {
          svg: '2',
          title: 'Корпоративный сайты',
          description: 'Корпоративный сайт – это сайт компании, ее официальное виртуальное представительство в интернете.'
        },
        {
          svg: '3',
          title: 'Интернет магазины',
          description: 'Мы создаем интернет-магазины на готовых движках, а также уникальные магазины, подключаем национальные и зарубежные способы оплаты.'
        },
        {
          svg: '4',
          title: 'Уникальная Веб-разработка',
          description: 'В зависимости от сложности Вашей задачи мы можем разработать корпоративный веб-сайт, портал или торговую площадку.'
        },
        {
          svg: '5',
          title: 'Мобильные приложения',
          description: 'Разработка мобильных приложений. Дизайн — прототипирование, программирование и тех поддержка.'
        },
        {
          svg: '6',
          title: 'Создание Телеграм ботов',
          description: 'Нужен Telegram-бот? Любая сложность, архитектура и алгоритмы работы ботов.'
        },
        {
          svg: '7',
          title: 'Графический дизайн',
          description: 'Уникальные логотипы, формирование брендбука и ребрендинг.'
        },
        {
          svg: '8',
          title: 'Продивижения в соц. сетях',
          description: 'Профессиональное ведение страниц, грамотная настройка таргетированной рекламы.'
        },
      ]
    }
  }
}
</script>

<style scoped>
</style>
