<template>
  <div>
    <Banner />
    <WhoAreWe />
    <WhatAreWeDoing />
    <Video />
    <WhatDoWeOffer />
    <Clients />
    <OurContacts />
  </div>
</template>

<script>
import Banner from "@/layouts/Banner";
import WhoAreWe from "@/layouts/WhoAreWe";
import WhatAreWeDoing from "@/layouts/WhatAreWeDoing";
import Video from "@/layouts/Video";
import WhatDoWeOffer from "@/layouts/WhatDoWeOffer";
import Clients from "@/layouts/Clients";
import OurContacts from "@/layouts/OurContacts";
import UpArrow from "@/components/upArrow";
export default {
  name: 'Home',
  components: {OurContacts, Clients, WhatDoWeOffer, Video, WhatAreWeDoing, WhoAreWe, Banner},
}
</script>

<style>
@media (max-width: 993px) {
  .banner-info {
    text-align: center;
  }
  .banner-img {
    display: none;
  }
  .feature {
    padding-bottom: 0!important;
    text-align: center;
  }
  .feature-description {
    font-size: 20px!important;
  }
  .feature:last-child {
    flex-direction: column-reverse;
  }
  .contact-input {
    width: 100%;
  }
  .contact-input button {
    margin-bottom: 1rem;
  }
  .contact-address {
    text-align: center;

  }
  .social-icons {

  }
}
@media (max-width: 498px) {
  .feature-img,
  .feature-img img{
    width: 100% !important;
  }
  .banner-title {
    font-size: 36px;
  }
}
</style>
