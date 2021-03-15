<template>
    <div class="position">
      <span class="iconfont position__icon">&#xe619;</span>
      北京理工大学国防科技园2号楼10层
      <span class="iconfont position__notice">&#xe628;</span>
    </div>
    <div class="search">
      <span class="iconfont">&#xe613;</span>
      山姆会员商店优惠产品
    </div>
    <div class="banner">
      <img
        class="banner__img"
        src="http://www.dell-lee.com/imgs/vue3/banner.jpg"
      />
    </div>
    <div class="icons">
      <div class="icons__item"
      v-for="item in iconList" :key="item.id"
      >
        <img
          :src="`http://www.dell-lee.com/imgs/vue3/${item.urlKeyword}.png`"
          class="icons__item__img"
        />
        <p class="icons__item__desc">{{ item.desc }}</p>
      </div>
    </div>
    <div class="gap"></div>
</template>

<script>
export default {
  name: 'StaticPart',
  setup () {
    const iconList = [
      {
        id: 1,
        urlKeyword: '超市',
        desc: '超市便利'
      },
      {
        id: 2,
        urlKeyword: '菜市场',
        desc: '菜市场'
      },
      {
        id: 3,
        urlKeyword: '水果店',
        desc: '水果店'
      },
      {
        id: 4,
        urlKeyword: '鲜花',
        desc: '鲜花绿植'
      },
      {
        id: 5,
        urlKeyword: '医药健康',
        desc: '医药健康'
      },
      {
        id: 6,
        urlKeyword: '家居',
        desc: '家居时尚'
      },
      {
        id: 7,
        urlKeyword: '蛋糕',
        desc: '烘培蛋糕'
      },
      {
        id: 8,
        urlKeyword: '签到',
        desc: '签到'
      },
      {
        id: 9,
        urlKeyword: '大牌免运',
        desc: '大牌免运'
      },
      {
        id: 10,
        urlKeyword: '红包',
        desc: '红包套餐'
      }
    ]
    return {
      iconList
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../../style/viriables.scss";
@import "../../style/mixins.scss";

.position {
  position: relative;
  padding: 0.16rem 0.24rem 0.15rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  color: $content-fontcolor;
  @include ellipsis;
  .position__icon {
    position: relative;
    top: 0.01rem;
    font-size: 0.2rem;
  }
  .position__notice {
    position: absolute;
    font-size: 0.2rem;
    right: 0;
    top: 0.17rem;
  }
}
.search {
  margin-bottom: 0.12rem;
  line-height: 0.32rem;
  background-color: #f5f5f5;
  color: #b7b7b7;
  border-radius: 0.16rem;
  font-size: 0.14rem;
  .iconfont {
    position: relative;
    top: 0.01rem;
    display: inline-block;
    padding: 0 0.1rem 0 0.16rem;
    font-size: 0.16rem;
  }
}
.banner {
  height: 0;
  overflow: hidden;
  padding-bottom: 25.4%;
  &__img {
    width: 100%;
  }
}
.icons {
  display: flex;
  flex-wrap: wrap;
  margin-top: 0.16rem;
  &__item {
    width: 20%;
    &__img {
      display: block;
      width: 0.4rem;
      height: 0.4rem;
      margin: 0 auto;
    }
    &__desc {
      margin: 0.06rem 0 0.16rem 0;
      text-align: center;
      color: $content-fontcolor;
    }
  }
}
.gap {
  height: 0.1rem;
  background-color: $content-bgColor;
  margin: 0 -0.18rem;
}
</style>
