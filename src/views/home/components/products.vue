<template>
  <div class="prod-box" v-for="item in cardLists" :key="item.id">
    <div class="imgLink">
      <a href="#"><img :src="item.asset" alt="图片无法显示" class="pic"></a>
    </div>
    <div class="nums">
      <span style="color: red;">收藏人数：{{item.collectNums}}</span>
      <span style="color: red;">总浏览：{{item.viewNums}}</span>
    </div>
    <div>
      <p class="review"><a href="#">{{item.title}}</a></p>
    </div>
    <div class="appraise">
      {{item.description}}
    </div>
    <div class="info">
      <del>{{item.originPrice}}</del>
      <span>￥{{item.price}}</span>
    </div>
  </div>
</template>

<script>
import cardLists from '../data/products.json'
export default {
  setup() {
    return {
      cardLists,
    }
  },
}
</script>

<style scoped>
a {
  color: rgb(0, 0, 0);
  text-decoration: none;
}

.prod-box {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 20px;
  width: 360px;
  height: 415px;
  text-align: start;
  background-color: white;
}

.imgLink {
  height: 200px;
  overflow: hidden;
}
.pic {
  width: 100%;
}

.nums,
.review,
.appraise {
  padding: 0 28px;
}

.nums {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 30px;
  width: 100%;
  font-size: 12px;
}

.review {
  margin: 0;
  font: 16px Helvetica Neue, Helvetica, Arial, Microsoft Yahei, Hiragino Sans GB, Heiti SC,
    WenQuanYi Micro Hei, sans-serif;
}

.appraise {
  color: #b0b0b0;
  font: 12px Helvetica Neue, Helvetica, Arial, Microsoft Yahei, Hiragino Sans GB, Heiti SC,
    WenQuanYi Micro Hei, sans-serif;
}

.info {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  margin-bottom: 15px;
  padding: 0 28px;
  width: 100%;
  font-size: 14px;
}
.info del {
  color: #d85248;
  margin-right: 5px;
}
.info span {
  color: #62e19c;
}
</style>