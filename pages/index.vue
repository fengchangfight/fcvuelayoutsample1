<template>
  <section class="container">
    <el-container style="height: 100%">
      <el-container>
        <div style="background-color:#002641;border:none;">
          <div class="logo">
            <img width="62px" height="60px;" src="/logo.png" />
          </div>
          <el-menu
            default-active="2"
            class="el-menu-vertical"
            @open="handleOpen"
            @close="handleClose"
            :collapse="isCollapse"
            background-color="#002641"
            text-color="white"
          >
            <el-submenu class="el-submenu-vertical" index="1">
              <template slot="title">
                <i class="el-icon-star-on"></i>
                <span slot="title">原始数据</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="1-1">item one</el-menu-item>
                <el-menu-item index="1-2">item two</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu class="el-submenu-vertical" index="2">
              <template slot="title">
                <i class="el-icon-star-off"></i>
                <span slot="title">矫正数据</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="1-1">item one</el-menu-item>
                <el-menu-item index="1-2">item two</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu class="el-submenu-vertical" index="4">
              <template slot="title">
                <i class="el-icon-document"></i>
                <span slot="title">测试集</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="1-1">item one</el-menu-item>
                <el-menu-item index="1-2">item two</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu class="el-submenu-vertical" index="4">
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
          <el-header>
            <label
              v-if="!isCollapse"
              style="margin-left:10px;"
              @click="toggleCollapse()"
              class="el-icon-arrow-left toggle-side"
            ></label>
            <label
              v-if="isCollapse"
              style="margin-left:10px;"
              @click="toggleCollapse()"
              class="el-icon-arrow-right toggle-side"
            ></label>
          </el-header>
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
  methods: {
    toggleCollapse() {
      this.isCollapse = !this.isCollapse
    }
  }
}
</script>

<style>
.container {
  height: 100vh;
}
.el-header,
.el-footer {
  background-color: white;
  color: #333;
  text-align: left;
  line-height: 60px;
}

.el-main {
  background-color: gray;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}
.el-menu-vertical {
  border: none;
}
.el-menu-vertical:not(.el-menu--collapse) {
  min-height: 200px;
}
.logo {
  background-color: #002641;
  min-height: 60px;
  display: flex;
}
.toggle-side:hover {
  cursor: pointer;
}
</style>
