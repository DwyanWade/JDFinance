<template lang="html">
  <div class="">
    <Heador/>
    <Slider/>
    <Ada/>
    <Pmoney/>
    <Adb/>
    <Finance/>
    <Footor/>
    <Navbar/>
  </div>
</template>

<script>
import Heador from '../public/header.vue';
import Slider from './mslider.vue';
import Ada from './ada.vue';
import Pmoney from './pmoney.vue';
import Adb from './adb.vue';
import Finance from './finance.vue';
import Footor from '../public/footer.vue';
import Navbar from '../public/navbar.vue';
export default {
  components: {
    Heador,
    Slider,
    Ada,
    Pmoney,
    Adb,
    Finance,
    Footor,
    Navbar,
  }
}
</script>
