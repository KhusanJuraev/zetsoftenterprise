<template>
  <div
    @click.passive="scrollTop"
    class="up-arrow position-fixed d-flex rounded-circle visible"
  >
    <BIconArrowUpCircle />
  </div>
</template>

<script>
import {BIconArrowUpCircle} from 'bootstrap-vue'
export default {
  name: "upArrow",
  components: {
    BIconArrowUpCircle
  },
  methods: {
    scrollTop: () => {
      window.scroll({
        top: 0,
        left: 0,
        behavior: 'smooth'
      })
    },
  },
  mounted: function () {
      window.addEventListener('scroll', () => {
        if (scrollY > 400) {
          console.log(scrollY);
          document.querySelector('.up-arrow').classList.add('visible');
        } else {
          document.querySelector('.up-arrow').classList.remove('visible');
        }
      })
  }
}
</script>

<style scoped>
.up-arrow {
  bottom: 20px;
  right: 20px;
  z-index: 1001;
  color: #0055F3;
  font-size: 42px;
  background: #fff;
  padding: 2px;
  cursor: pointer;
  opacity: 0;
  visibility: hidden;
  transition: .2s ease-in;
}
.visible {
  opacity: 1;
  visibility: visible!important;
}
</style>
