<template>
  <section id="whoAreWe">
      <div class="container">

        <Title v-bind:text="text" v-bind:title="title"/>

        <div class="features">

          <div class="feature d-flex justify-content-around align-items-center pb-5">
            <kinesis-element strength="10">
              <div class="feature-img">
                <kinesis-element strength="5">
                  <img src="../assets/img/feature-img1.png" alt="">
                </kinesis-element>
              </div>
            </kinesis-element>
            <div class="feature-content w-50">
              <p class="feature-description">
                <span>ZETSOFT</span> — инновационная IT компания в Ташкенте, работающая по методологиям
                Scrum/Kanban, предлагает своим клиентам широкий спектр услуг по комплексной
                поддержке бизнеса клиентов на долгосрочной основе.
              </p>
            </div>
          </div>

          <div class="feature d-flex justify-content-around align-items-center pt-5">
            <div class="feature-content w-50">
              <p class="feature-description">
                <span>Мы</span> не просто делаем сайты и мобильные приложения, наша стратегия — быть лучшими в создании
                медиапространств, где эти сайты и приложения будут работать, а мы сможем привлечь аудиторию,
                обеспечить ее стабильный интерес и рост.
              </p>
            </div>
            <kinesis-element strength="10">
              <div class="feature-img">
                <kinesis-element strength="5">
                  <img src="../assets/img/feature-img2.png" alt="">
                </kinesis-element>
              </div>
            </kinesis-element>
          </div>

        </div>
      </div>
  </section>
</template>

<script>
import Title from "@/components/Title"
import { KinesisContainer, KinesisElement} from 'vue-kinesis'


export default {
  name: "WhoAreWe",
  components: {
    Title,
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement
  },
  data() {
    return {
      title: "КТО МЫ?",
      text: `Мы предоставляем креатив решения, чтобы превратить ваш идеи в цифровую реальность`
    }
  }
}
</script>

<style scoped>
.feature-img {
  position: relative;
  background: #FFFFFF;
  box-shadow: 0 12px 50px rgba(0, 0, 0, 0.1);
  border-radius: 44px;
  width: 450px;
  height: 300px;
  display: flex;
  justify-content: center;
  align-content: center;
}
.feature-img img {
  width: 480px;
  height: 318px;
}
.feature-description {
  font-weight: 300;
  font-size: 24px;
  line-height: 150%;
  color: #1A2863;
}
.feature-description span {
  font-weight: 500;
}
</style>
