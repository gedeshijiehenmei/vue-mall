<template>
  <div id="category">
    <nav-bar class="nav-bar"><div slot="center">商品分类</div></nav-bar>
  </div>
</template>
<script>
import NavBar from '../../components/common/navbar/Navbar'
export default {
  name: 'category',
  components: {
    NavBar
  }
}
</script>
<style lang="less" scoped>
#category {
  /*position: relative;*/
  height: 100vh;
}

.nav-bar {
  background-color: var(--color-tint);
  font-weight: 700;
  color: #fff;
}
</style>
