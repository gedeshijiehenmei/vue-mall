<template>
  <div id="cart">
    <nav-bar class="nav-bar"
      ><div slot="center">购物车({{ cartCount }})</div></nav-bar
    >
  </div>
</template>
<script>
import NavBar from '../../components/common/navbar/Navbar'
export default {
  name: 'cart',
  data () {
    return {
      cartCount: 0
    }
  },
  components: {
    NavBar
  }
}
</script>
<style lang="less" scoped>
#cart {
    /*position: relative;*/
    height: 100vh;
  }

  .nav-bar {
    background-color: var(--color-tint);
    font-weight: 700;
    color: #fff;
  }
  </style>
