<template>
  <section class="overflow-hidden">
    <kinesis-container>
      <div class="container">
        <page-title
          title="ЧТО МЫ ДЕЛАЕМ..."
          img="pageImg2"
        />
        <div class="services-info text-center">
          <h3>Мы делаем то, что любим и любим то, что делаем...</h3>
          <p>
            Помогаем клиентам построить результативный бизнес при помощи интернет-маркетинга.
            Проектируем и создаем продающие лендинги, корпоративные сайты, интернет-магазины,
            сайты с индивидуальным решением, мобильные приложения, телеграм боты. Также мы
            предоставляем услуги профессионального графического дизайна, на случай его отсутствия.
            Мы делаем хорошую рекламу в Интернете и в социальных сетях Facebook, Instagram с
            максимальным эффектом. Мы заботимся, чтобы реализованные нами проекты приносили успех своим владельцам.
          </p>
        </div>
        <div class="services-cards d-flex justify-content-around flex-wrap align-items-center">
          <ServicesCard
            v-for="service of services"
            :svg="service.svg"
            :title="service.title"
            :description="service.description"
          />
          <p class="text-center text-dark"><i>
            *Окончательная стоимость услуг и срок разработки может варьироваться исходя из ваших потребностей, <br>
            пожеланий и сложности технического задания.
          </i></p>
        </div>
        <OrderProject />
      </div>
    </kinesis-container>
  </section>
</template>

<script>
import { KinesisContainer, KinesisElement} from 'vue-kinesis'
import PageTitle from "@/components/pageTitle";
import ServicesCard from "@/components/ServicesCard";
import OrderProject from "@/components/OrderProject";
export default {
  name: "About",
  components: {
    OrderProject,
    ServicesCard,
    PageTitle,
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement
  },
  data () {
    return {
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
.services-cards {
  margin: 120px 0 50px;
}
.services-info h3{
  font-weight: 900;
  font-size: 32px;
  color: #061552;
}
.services-info p {
  font-weight: normal;
  font-size: 20px;
  margin-top: 20px;
  color: #1A2863;
}
@media (max-width: 998px) {
  .services-info h3 {
    font-size: 24px;
  }
  .services-info p {
    font-size: 18px;
  }
  .services-cards {
    margin: 3rem 0;
  }
  .order-project {
    padding-top: 0;
  }
}
</style>
