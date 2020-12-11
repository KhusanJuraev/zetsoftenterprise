<template>
  <section class="video-section position-relative" id="video">
    <div class="container d-flex justify-content-center align-items-center">
      <div class="video-item overflow-hidden position-relative">
        <b-embed
          type="iframe"
          aspect="16by9"
          src="https://www.youtube.com/embed/VGV09dUwXo4"
          allowfullscreen
          class="video"
        ></b-embed>
      </div>
    </div>
  </section>
</template>

<script>
export default {
name: "Video"
}
</script>

<style scoped>
.video-section:before {
  content: '';
  position: absolute;
  background-color: rgba(0, 85, 243, 1);
  bottom: 0;
  height: 50%;
  width: 100%;
}
.video-item {
  border-radius: 44px;
  width: 600px;
  height: 400px;
}
.video {
  position: absolute;
  width: 100%;
  height: 100%;
  border-radius: 44px;
}
</style>
