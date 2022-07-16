<template>
  <router-view></router-view>
  <div class="docker">
    <div class="docker__item docker__item--active">
      <i class="iconfont icon-homefill"></i>
      <div class="title">首页</div>
    </div>
    <div class="docker__item">
      <i class="iconfont icon-cart"></i>
      <div class="title">购物车</div>
    </div>
    <div class="docker__item">
      <i class="iconfont icon-order"></i>
      <div class="title">订单</div>
    </div>
    <div class="docker__item">
      <i class="iconfont icon-my"></i>
      <div class="title">我的</div>
    </div>
  </div>
</template>
<!-- https://www.fastmock.site/mock/ae8e9031947a302fed5f92425995aa19/jd/api/user/register -->

<script>
import { reactive } from 'vue'
export default {
  name: 'App',
  setup() {
    const navList = reactive([])
    return { navList }
  }
}
</script>

<style lang="less">
.docker {
  display: flex;
  align-items: center;
  position: absolute;
  bottom: 0;
  left: 0;
  padding: 0 0.18rem;
  box-sizing: border-box;
  height: 0.49rem;
  width: 100%;
  border-top: 1px solid #f1f1f1;
  .docker__item {
    flex: 1;
    text-align: center;
    &.docker__item--active {
      color: #1fa4fc;
    }
    .iconfont {
      display: block;
      font-size: 0.18rem;
    }
    .title {
      font-size: 20px;
      transform: scale(0.5, 0.5);
      transform-origin: center;
    }
  }
}
</style>
