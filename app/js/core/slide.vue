<template>
  <section :class="[cname]">
      <swiper :options="options" :not-next-tick="options.notNextTick">
          <swiper-slide v-for="item in items" :key="item.src">
              <router-link :to="{name:item.href}">
                  <img :src="item.src" alt="">
              </router-link>
          </swiper-slide>

          <div class="swiper-pagination" slot="pagination" v-if="options.pagination"></div>
      </swiper>
  </section>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
    props:{
        cname:{
            type:String,
            defualt:''
        },
        items:{
            type:Array,
            default:function(){
                return [];                
            }
        }
        ,
        options:{
            type:Object,
            default:function(){
                return {
                    autoplay:true,
                    loop:true,
                    pagination:{
                        el:".swiper-pagination"
                    },
                    notNextTick:false,
                }
            },
        }
    },
    data () {
        return {
        };
    },

    components: {
        swiper:swiper,
        SwiperSlide:swiperSlide
    },

    computed: {},

    methods: {}
}

</script>
<style lang='scss'>
@import "~swiper/dist/css/swiper.css";
</style>