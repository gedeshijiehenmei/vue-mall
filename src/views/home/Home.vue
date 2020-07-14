<template>
  <div id="home">
    <nav-bar class="nav-bar"><div slot="center">购物街</div></nav-bar>
    <!-- <tab-control
      v-show="isTabFixed"
      class="fixed"
      @itemClick="tabClick"
      :titles="['流行', '新款', '精选']"
    ></tab-control> -->
    <div class="main">
      <home-swiper :banners="banners"></home-swiper>
      <recommend-view :recommend="recommend">></recommend-view>
      <feature-view></feature-view>
      <tab-control :titles="['流行', '新款', '精选']"></tab-control>
      <ul><li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      <li>aaaaaaaaaaaaaaa</li>
      </ul>
    </div>
  </div>
</template>
<script>
import NavBar from '../../components/common/navbar/Navbar'
import HomeSwiper from './childComps/HomeSwiper'
import RecommendView from './childComps/RecommendView'
import FeatureView from './childComps/FeatureView'
import TabControl from './childComps/TabControl'
import { getHomeMultidata } from '../../network/home'
export default {
  name: 'home',
  data () {
    return {
      banners: [],
      recommend: []
    }
  },
  components: {
    NavBar,
    HomeSwiper,
    RecommendView,
    FeatureView,
    TabControl
  },
  created () {
    getHomeMultidata().then(res => {
      this.banners = res.data.banner.list
      this.recommend = res.data.recommend.list
      console.log(res)
    })
  }
}
</script>
<style lang="less" scoped>
#home {
  /*position: relative;*/
  height: 100vh;
}
.nav-bar {
  background-color: var(--color-tint);
  font-weight: 700;
  color: #fff;
  position: fixed !important;
  top: 0 !important;
  width: 100% !important;
}
.main{
margin-top: 40px;
}
.tab-control {
  position: sticky;
  top: 40px;
}
</style>
