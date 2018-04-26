<template>
  <div id="app">
    <div v-if="recommends.length" class="slider-wrapper">
      <slider>
        <div v-for="(item,index) in recommends" :key="index">
          <a :href="item.linkUrl">
            <img :src="item.picUrl">
          </a>
        </div>
      </slider>
    </div>
  </div>
</template>

<script>
import slider from './components/slider/slider'
import src1 from "./assets/img/1.jpg"
import src2 from "./assets/img/2.jpg"
import src3 from "./assets/img/3.jpg"
export default {
  data() {
    return {
      recommends: [
        {
          linkUrl: "1111",
          picUrl: src1
        },
        {
          linkUrl: "2222",
          picUrl: src2
        },
        {
          linkUrl: "3333",
          picUrl: src3
        }
      ]
    }
  },
  components: {
    slider
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
.slider-wrapper
  position: relative
  width: 100%
  overflow: hidden
       
</style>
