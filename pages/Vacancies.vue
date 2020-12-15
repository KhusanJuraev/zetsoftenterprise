<template>
  <section class="overflow-hidden">
    <kinesis-container>
      <div class="container">
        <page-title
          title="Отправка резюме..."
          img="pageImg3"
        />
        <div class="vacancies">
          <h3 class="text-center">Мы очень рады вас пригласить на собеседование</h3>

          <div class="vacancies-form d-flex">
            <div class="contact-input">
              <b-form-input
                id="`type-text`"
                v-model="values.name"
                type="text"
                class="mb-4"
                placeholder="Ваше имя"
              ></b-form-input>
              <b-form-input
                id="`type-tel}`"
                v-model="values.telephone"
                type="tel"
                class="mb-4"
                placeholder="Телефон"
              ></b-form-input>
              <b-form-textarea
                id="textarea"
                v-model="values.text"
                placeholder="Расскажите о себе"
                rows="3"
                max-rows="6"
              ></b-form-textarea>
              <b-form-file v-model="file" class="mt-3" plain></b-form-file>
            </div>
            <div class="contact-checkbox px-4">
              <span>Выберите технологии и языки программирование которорые вы работали и знаете что это такое</span>
              <Checkbox
                :selected="selected"
                :options="options"
                :flex="style"
                class="checkbox-group"
              />
            </div>
          </div>
          <b-button pill class="px-4 py-2 mt-4" variant="primary">Отправить</b-button>

        </div>
        <OrderProject />
      </div>
    </kinesis-container>
  </section>
</template>

<script>
import { KinesisContainer, KinesisElement} from 'vue-kinesis'
import PageTitle from "@/components/pageTitle";
import Checkbox from "@/components/Checkbox";
import OrderProject from "@/components/OrderProject";
export default {
  name: "Vacancies",
  components: {
    OrderProject,
    Checkbox,
    PageTitle,
    'kinesis-container': KinesisContainer,
    'kinesis-element': KinesisElement
  },
  data() {
    return {
      values: {
        name: "",
        telephone: "",
        text: "",
      },
      file: null,
      options: [
        { value: "PHP", text: "PHP" },
        { value: "JavaScript", text: "JavaScript" },
        { value: "Vue.js", text: "Vue.js" },
        { value: "Yii2", text: "Yii2" },
        { value: "Laravel", text: "Laravel" },
        { value: "Git", text: "Git" },
        { value: "Mysql", text: "Mysql" },
        { value: "PostgreSQL", text: "PostgreSQL" },
        { value: "HTML", text: "HTML" },
        { value: "Sass or Less", text: "Sass or Less" },
        { value: "Android SDK", text: "Android SDK" },
        { value: "Swift", text: "Swift" },
        { value: "RESTful API", text: "RESTful API" },
        { value: "NGINX", text: "NGINX" },
        { value: "Redis, Memcached", text: "Redis, Memcached" },
        { value: "Docker", text: "Docker" },
        { value: "Node.js", text: "Node.js" },
        { value: "ООП", text: "ООП" },
        { value: "MongoDB", text: "MongoDB" },
        { value: "Другое", text: "Другое" },
      ],
      types: ["text", "tel"],
      style: "flex-wrap",
      selected: [],
    }
  }
}
</script>

<style scoped>
.contact-input {
  max-width: 450px;
}
.checkbox-group {
  display: grid!important;
  grid-template-rows: 1fr 1fr 1fr 1fr;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-gap: 5px;
  margin-top: 20px;
}
.vacancies h3 {
  font-weight: 900;
  font-size: 36px;
  color: #061552;
  margin: 120px 0 60px;
}
.vacancies span {
  font-size: 18px;
  color: #222;
}
@media (max-width: 992px) {
  .vacancies-form {
    flex-wrap: wrap;
  }
  .contact-input {
    width: 100%;
    margin-bottom: 1rem;
  }
}
@media (max-width: 590px) {
  .vacancies h3 {
    font-size: 24px;
  }
  .checkbox-group {
    display: grid!important;
    grid-template-rows: 1fr 1fr;
    grid-template-columns: 1fr 1fr;
    grid-gap: 5px;
    margin-top: 20px;
  }
}
</style>
