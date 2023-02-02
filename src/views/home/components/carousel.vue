<template>
  <el-carousel height="477" indicator-position="outside">
    <el-carousel-item v-for="item in carouselLists" :key="item.id">
      <a href="javascript:;">
        <img :src="item.asset" alt="" style="max-width: 850px; height: 100%;">
      </a>
    </el-carousel-item>
  </el-carousel>
</template>

<script>
import carouselLists from '../data/carousel.json'
export default {
  setup() {
    return {
      carouselLists,
    }
  },
}
</script>

<style lang="scss" scoped>
.el-carousel__item {
  background-color: #c8c8c8;
}
.el-carousel,
.el-carousel--horizontal {
  width: 850px;
  height: 480px;
}
::v-deep .el-carousel__container {
  position: relative;
  width: 850px;
  height: 450px !important;
}
</style>