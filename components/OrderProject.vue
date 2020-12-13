<template>
  <div class="order-project d-flex flex-column justify-content-center align-items-center text-center">
    <h3>Доверьте Ваш Бизнес Нам!</h3>
    <p>Оставьте заявку, и наш менеджер свяжется с Вами в ближайшее время</p>
    <nuxt-link to="/contacts" size="lg" class="rounded-pill">Заказать проект</nuxt-link>
  </div>
</template>

<script>
export default {
  name: "OrderProject"
}
</script>

<style scoped>
.order-project {
  padding: 100px 0;
}
.order-project h3 {
  font-weight: 800;
  font-size: 36px;
  color: #061552;
}
.order-project p {
  font-weight: 800;
  font-size: 18px;
  background: #1A2863;
  padding: 0 10px;
  color: #fff;
  margin-top: 10px;
}
.order-project a {
  background: #0047FF;
  color: #fff;
  padding: 20px 25px;
  margin-top: 20px;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.3);
  text-decoration: none;
}
.order-project a:hover {
  box-shadow: 0 5px 25px rgba(0, 0, 0, 0.5);
  background: #0241de;
}
</style>
