<template>
  <div class="layout-aside">
     <div class="title">
        <img src="../../assets/img/x2.jpg" alt="">
     </div>
     <!-- 加上：才不是字符串，才真正的开启了路由模式  简写router，直接写个router效果是一样的 -->
     <!-- 使用属性 -->
     <el-menu  :collapse="collapse" :router="true" background-color="#323745" text-color="#adafb5">
        <el-menu-item index="/home">
           <i class="el-icon-s-home"></i>
           <span>首页</span>
        </el-menu-item>
        <el-submenu index='1'>
          <template slot="title">
            <i class="el-icon-s-grid"></i>
            <span>内容管理</span>
          </template>
          <el-menu-item index='/home/publish'>发布文章</el-menu-item>
          <el-menu-item index='/home/articles'>文章列表</el-menu-item>
          <el-menu-item index='/home/comment'>评论列表</el-menu-item>
          <el-menu-item index='/home/material'>素材管理</el-menu-item>
        </el-submenu>
        <el-submenu index='2'>
          <template slot="title">
            <i class="el-icon-s-opportunity"></i>
            <span>粉丝管理</span>
          </template>
          <el-menu-item index='/home/picture'>图文数据</el-menu-item>
          <el-menu-item index='/home/fansinfo'>粉丝概况</el-menu-item>
          <el-menu-item index='/home/fansphoto'>粉丝画像</el-menu-item>
          <el-menu-item index='/home/fanslist'>粉丝列表</el-menu-item>
        </el-submenu>
        <el-menu-item index='/home/account'>
           <i class="el-icon-user-solid"></i>
           <span>账户信息</span>
        </el-menu-item>
     </el-menu>
  </div>
</template>

<script>
// 接收属性
export default {
  props: ['collapse']

}
</script>

<style lang="less" scoped>
.layout-aside{
  background-color: #242f32;
  width: 230px;
  height: 100vh;
   .title{
     text-align: center;
     padding: 10px 0;
      img{
        width: 50px;
        height: 35px;

      }
   }
   .el-menu{
     border: none;
   }
}

</style>
