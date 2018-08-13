<template>
    <div>
        <!-- <heador><heador> -->
          <heador></heador>
          <hslider></hslider>
          <novice></novice>
          <borrow></borrow>
    </div>
</template>

<script>
import heador from '../public/header.vue';
import hslider from './hslider.vue';
import Novice from './novice.vue';
import Borrow from './borrow.vue';
export default {
  components:{
    heador,
    hslider,
    Novice,
    Borrow,
  }
}
</script>

<style lang="scss" module>
@import "../../css/reset.scss";
</style>
