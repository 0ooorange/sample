<template>
  <ul class="aside-box">
    <li class="aside-item" v-for="item in asideMenuLists" :key="item.id">
      <div class="aside-item-content">{{item.type}}</div>
      <div class="aside-item-nums">{{item.children.length}}</div>
    </li>
  </ul>
</template>

<script>
import asideMenuLists from '../data/aside.json'
export default {
  setup() {
    return {
      asideMenuLists,
    }
  },
}
</script>
<style lang="scss" scoped>
.aside-box {
  margin: 0;
  padding: 0;
  width: 234px;
  height: 343px;

  font-size: 13px;
  font-family: inherit;
  font-weight: 500;
  list-style: none;

  background-color: white;
}
.aside-item {
  height: 42px;
  color: #384047;
  border-bottom: 1px solid rgba(211, 211, 211, 0.6);
  transition: all 300ms;
  cursor: pointer;
}
.aside-item:hover {
  padding: 0 0 0 10px;
  .aside-item-nums {
    color: white;
    background-color: rgb(46, 216, 123);
  }
}
.aside-item-content {
  display: inline-block;
  line-height: 42px;
  cursor: pointer;
}
.aside-item-nums {
  display: inline-block;
  margin-left: 10px;
  width: 20px;
  height: 20px;
  line-height: 20px;
  color: #BFBFBF;
  border-radius: 3px;
  cursor: pointer;
}
</style>