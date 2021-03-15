<template>
  <div class="docker">
    <span
    v-for="(item, index) in dockerList" :key="item"
    :class="{'docker__item': true, 'docker__item--active': index === 0}"
    >
      <div class="iconfont" v-html="item.icon"></div>
      <div class="docker__title">{{item.text}}</div>
    </span>
  </div>
</template>

<script>
export default {
  name: 'Docker',
  setup () {
    const dockerList = [
      {
        icon: '&#xe625;',
        text: '首页'
      },
      {
        icon: '&#xe638;',
        text: '购物车'
      },
      {
        icon: '&#xe60d;',
        text: '订单'
      },
      {
        icon: '&#xe78b;',
        text: '我的'
      }
    ]

    return {
      dockerList
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../../style/viriables.scss";

.docker {
  display: flex;
  box-sizing: border-box;
  position: absolute;
  padding: 0 0.18rem;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 0.49rem;
  border-top: 0.01px solid $content-bgColor;
  color: $content-fontcolor;
  &__item {
    flex: 1;
    text-align: center;
    &--active {
      color: #1fa4fc;
    }
    .iconfont {
      margin: 0.07rem 0 0.02rem 0;
      font-size: 0.2rem;
    }
  }
  &__title {
    font-size: 0.2rem;
    transform: scale(0.5, 0.5);
    transform-origin: center top;
  }
}
</style>
