<template>
  <div id="profile">
    <nav-bar class="nav-bar"><div slot="center">个人中心</div></nav-bar>
  </div>
</template>
<script>
import NavBar from '../../components/common/navbar/Navbar'
export default {
  name: 'profile',
  components: {
    NavBar
  }
}
</script>
<style lang="less" scoped>
#profile {
  /*position: relative;*/
  height: 100vh;
}

.nav-bar {
  background-color: var(--color-tint);
  font-weight: 700;
  color: #fff;
}
</style>
