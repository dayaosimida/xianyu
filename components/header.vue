<template>
    <header class="header">
        <el-row type="flex" justify="space-between" class="main">

            <!-- logo -->
            <div class="logo">
                <nuxt-link to="/">
                    <img src="http://157.122.54.189:9093/images/logo.jpg" alt="">
                </nuxt-link>
            </div>

            <!-- 菜单栏 -->
            <el-row type="flex" class="navs">
                <nuxt-link to="/">首页</nuxt-link>
                <nuxt-link to="/post">旅游攻略</nuxt-link>
                <nuxt-link to="/hotel">酒店</nuxt-link>
                <nuxt-link to="/air">国内机票</nuxt-link>  
            </el-row>

            <!-- 登录/用户信息 -->
            <el-row type="flex" align="middle">

                <!-- 如果用户存在则展示用户信息，用户数据来自store -->
                <el-dropdown v-if="false">
                    <el-row type="flex" align="middle" class="el-dropdown-link">
                        <nuxt-link to="#">
                            <img src="http://157.122.54.189:9093/images/pic_sea.jpeg"/>
                            用户名
                        </nuxt-link>
                        <i class="el-icon-caret-bottom el-icon--right"></i>
                    </el-row>
                    <el-dropdown-menu slot="dropdown">
                        <el-dropdown-item>
                           <nuxt-link to="#">个人中心</nuxt-link>
                        </el-dropdown-item>
                        <el-dropdown-item>
                            <div @click="handleLogout">退出</div> 
                        </el-dropdown-item>
                    </el-dropdown-menu>
                </el-dropdown>

                <!--        不存在用户信息展示登录注册链接 -->
                <nuxt-link to="/user/login" class="account-link" v-else>
                    登录 / 注册 
                </nuxt-link>
            </el-row>
        </el-row>
    </header>
</template>
<script>
export default {
    // 组件加载
    methods: {
        // 用户退出
        handleLogout(){},
    }
}
</script>
<style scoped lang="less">
  .container{
        width: 100%;
        height: 60px;
        line-height: 60px;
        border-bottom: 1px #ddd solid;
        box-shadow: 0 2px 2px #ddd;
    }
    .main{
        width: 1000px;
        margin: 0 auto;
    }
    .navs{
        flex:1;
        margin-left:10px;
        a{
            display: block;
            height: 60px;
            line-height: 60px;
            padding: 0 20px;
            box-sizing: border-box;
            &:hover{
                color: #409eff;
                border-bottom:5px #409eff solid;
            }
        }
        // 该class是nuxt会去自动匹配nuxt-link的to的值，如果url和to的值相等会自动加上下面的class
        .nuxt-link-exact-active{
            background: #409eff;
            color: #fff;
            &:hover{
                color: #fff;
            }
        }
    }
    
    .logo{
        padding-top: 9px;
        img {
            width:156px;
            height:42px;
            display: block;
        }
    }
    // 头像样式
    .el-dropdown-link img{
        width: 36px;
        height:36px;
        border-radius: 50%;
        vertical-align: middle;
        box-sizing: border-box;
        border:2px #fff solid;
        &:hover{
            border:2px #409eff solid;
        }
    }
</style>