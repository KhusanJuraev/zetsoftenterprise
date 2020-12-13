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
</style>
