<template>
  <div class="home-body">
    <el-container>
      <el-header>
        <Header />
      </el-header>
      <el-main>
        <div class="home-body-main">
          <span class="home-body-main-left"></span>
          <span class="home-body-main-contain">
            <Aside />
            <Carousel />
          </span>
          <span class="home-body-main-right"></span>
        </div>
        <div class="titleCard">
          <span class="card-content">优惠券</span>
          <el-button type="success" plain class="checkAllBtn">查看所有</el-button>
        </div>
        <div class="titleCard">
          <span class="card-content">全部商品</span>
          <el-button type="success" plain class="checkAllBtn">查看所有</el-button>
        </div>
        <div class="productCards">
          <Products />
        </div>
        <div class="titleCard">
          <span class="card-content">活跃的用户</span>
        </div>
      </el-main>
      <el-footer>
        <div class="sponsors">
          <img v-for="item in sponsorsList" :key="item.id" :src="item.asset" alt="" class="sponsorsImg">
        </div>
        <div class="footer">
          Copyright © 2017 . All rights moon.
        </div>
      </el-footer>
    </el-container>
    <el-backtop :right="100" :bottom="100" />
  </div>
</template>

<script>
// @ is an alias to /src
import { ref } from 'vue'
import Aside from './components/aside.vue'
import Header from './components/header.vue'
import Carousel from './components/carousel.vue'
import Products from './components/products.vue'
import sponsorsList from './data/sponsors.json'
import { Search } from '@element-plus/icons-vue'

export default {
  name: 'home',
  components: {
    Aside,
    Header,
    Carousel,
    Products
  },
  setup() {
    const input1 = ref('')
    return {
      input1,
      Search,
      sponsorsList
    }
  },
}
</script>
<style scoped>
.home-body {
  background-color: rgb(233, 235, 238);
}
.el-main {
  --el-main-padding: 0;
}
.el-header {
  height: auto;
  padding: 0;
  margin-bottom: 40px;
}
.el-footer {
  margin: 0;
  padding: 0;
}
/* 圣杯布局 */
.home-body-main {
  display: flex;
}
.home-body-main-left,
.home-body-main-right {
  width: 12%;
}
.home-body-main-contain {
  display: flex;
  flex: 1;
  justify-content: space-between;
}
.titleCard {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  margin-bottom: 20px;
  width: 76%;
  height: 62px;
  background-color: white;
}
.card-content {
  margin-left: 3%;
  font-size: 18px;
}
.checkAllBtn {
  font-size: 12px;
  margin-right: 3%;
}
.productCards {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 76%;
  margin: 0 auto;
}
.sponsors {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 133px;
  background-color: #314555;
}
.sponsorsImg {
  width: 55px;
  height: 33px;
  margin: 0 5px;
}
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60px;
  background-color: #1e2b35;
  color: #647d89;
}
</style>
