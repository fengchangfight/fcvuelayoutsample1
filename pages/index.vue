<template>
  <section class="container">
    <el-container style="height: 100%">
      <el-container>
        <div>
          <div class="logo">
            <img width="60px" height="60px;" src="/logo.png" />
            <h1
              style="color:white;margin-top:13px;font-size: 22px;font-weight: 600;"
            >
              数据治理
            </h1>
          </div>
          <el-menu
            default-active="2"
            class="el-menu-vertical"
            @open="handleOpen"
            @close="handleClose"
            :collapse="isCollapse"
          >
            <el-submenu index="1">
              <template slot="title">
                <i class="el-icon-star-on"></i>
                <span slot="title">原始数据</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="1-1">item one</el-menu-item>
                <el-menu-item index="1-2">item two</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu index="2">
              <template slot="title">
                <i class="el-icon-star-off"></i>
                <span slot="title">矫正数据</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="1-1">item one</el-menu-item>
                <el-menu-item index="1-2">item two</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu index="4">
              <template slot="title">
                <i class="el-icon-document"></i>
                <span slot="title">测试集</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="1-1">item one</el-menu-item>
                <el-menu-item index="1-2">item two</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu index="4">
              <template slot="title">
                <i class="el-icon-tickets"></i>
                <span slot="title">测试</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="1-1">常规测试</el-menu-item>
                <el-menu-item index="1-2">伴随测试</el-menu-item>
                <el-menu-item index="1-3">发布测试</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
          </el-menu>
        </div>
        <el-container>
          <el-header></el-header>
          <el-main></el-main>
        </el-container>
      </el-container>
    </el-container>
  </section>
</template>
<script>
export default {
  data() {
    return {
      isCollapse: false
    }
  },
  methods: {}
}
</script>

<style>
.container {
  height: 100vh;
}
.el-header,
.el-footer {
  background-color: #002641;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #d3dce6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
.el-menu-vertical:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
.logo {
  background-color: #002641;
  min-height: 60px;
  display: flex;
}
</style>
