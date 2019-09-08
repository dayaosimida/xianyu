<template>
  <div>
    <!-- 头部组件 -->
    <home-header />
   <!-- 内容占位组件 代替了坑 -->
    <nuxt />
    <!-- 尾部组件 -->
    <Footer />
  </div>
</template>
<script>
import HomeHeader from '@/components/header.vue'
import Footer from '@/components/footer.vue'
export default {
  // 注册组件
  components:{
    HomeHeader,
    Footer
  }
}
</script>
<style lang='less'>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*{
  margin: 0;
  padding: 0;
}
ul,li,ol{
  list-style:none;
}
a{
  text-decoration: none;
  color:inherit       
}
em,i{
  font-style: normal;
}
</style>
