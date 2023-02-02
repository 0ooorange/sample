<template>
  <div class="icons">
    <div class="icons-left"></div>
    <div class="icons-center">
      <div>
        <span>
          <el-icon>
            <QuestionFilled color="#2ed87b" />
          </el-icon>
          指南
        </span>
        <span>
          <el-icon>
            <Wallet color="#2ed87b" />
          </el-icon>
          兑换优惠券
        </span>
      </div>
      <div>
        <span>
          <el-icon>
            <Wallet color="#2ed87b" />
          </el-icon>
          优惠券
        </span>
        <span>
          <el-icon>
            <UserFilled color="#2ed87b" />
          </el-icon>
          游客
        </span>
        <span>
          <el-icon>
            <Lock color="#2ed87b" />
          </el-icon>
          登录
        </span>
        <span>
          <el-icon>
            <UserFilled color="#2ed87b" />
          </el-icon>
          注册
        </span>
      </div>
    </div>
    <div class="icons-right"></div>
  </div>
  <div class="search">
    <div class="search-left"></div>
    <a href="/" class="search-center-L">
      <img class="image" src="@/assets/logo.png" alt="">
    </a>
    <div class="search-center-C">
      <el-input v-model="input1" class="m-2" size="large" placeholder="输入关键字......" :suffix-icon="Search" />
    </div>
    <div class="search-center-R">
      <ShoppingTrolley style="width: 2rem; height: 2rem;" />
      <span>购物车</span>
      <Star style="width: 2rem; height: 2rem; margin-left: 8px;" />
      <span>收藏列表</span>
    </div>
    <div class="search-right"></div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.search {
  display: flex;
  align-items: center;
  padding: 30px 0;
  background-color: #fff;
}
.el-input {
  width: 500px;
}
.image {
  width: 250px;
}.icons {
  height: 46px;
  line-height: 46px;
  font-size: 12px;
}
.icons-center {
  display: flex;
  flex: 1;
  justify-content: space-between;
}
.icons-center span {
  margin: 0 5px;
}
.search-center-R {
  display: flex;
  align-items: center;
  font-size: 14px;
}
/* 圣杯布局 */
.icons {
  display: flex;
}
.icons-left,
.icons-right,
.search-left,
.search-right {
  width: 12%;
}
.icons-center,
.search-center-C {
  flex: 1;
}
</style>