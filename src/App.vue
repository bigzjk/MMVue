<template>
  <div id="app">
    <el-container>
      <el-header height="120px">
        <h1>Headdas头部头部Headdas头部头部Headdas头部头部Headdas头部头部</h1>
      </el-header>
      <el-container>
        <el-aside width="200px">
          <el-col>
            <h5>默认颜色</h5>
            <el-menu
              default-active="2"
              class="el-menu-vertical-demo"
              @open="handleOpen"
              @close="handleClose"
            >
              <el-submenu index="1">
                <template slot="title">
                  <i class="el-icon-location"></i>
                  <span>导航一</span>
                </template>
                <el-menu-item-group>
                  <template slot="title">分组一</template>
                  <router-link to="./">
                    <el-menu-item index="1-1">选项1</el-menu-item>
                  </router-link>

                  <el-menu-item index="1-2">选项2</el-menu-item>
                </el-menu-item-group>
                <el-menu-item-group title="分组2">
                  <el-menu-item index="1-3">选项3</el-menu-item>
                </el-menu-item-group>
                <el-submenu index="1-4">
                  <template slot="title">选项4</template>
                  <el-menu-item index="1-4-1">选项1567890987656789</el-menu-item>
                </el-submenu>
              </el-submenu>
              <router-link to="./about">
                <el-menu-item index="2">
                  <i class="el-icon-menu"></i>
                  <span slot="title">导航二</span>
                </el-menu-item>
              </router-link>
              <router-link to="./list">
                <el-menu-item index="3">
                  <i class="el-icon-document"></i>
                  <span slot="title">导航三</span>
                </el-menu-item>
              </router-link>
              <el-menu-item index="4">
                <i class="el-icon-setting"></i>
                <span slot="title">导航四</span>
              </el-menu-item>
            </el-menu>
          </el-col>
        </el-aside>
        <el-main>
          <router-view></router-view>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>
<script>
export default {
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
      return `${key} ${keyPath}`
    
    },
    handleClose(key, keyPath) {
      return `${key} ${keyPath}`
      // console.log(key, keyPath);
    }
  }
};
</script>
<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.el-container>.el-header{
  border-bottom: 1px solid #ededed;
}
</style>
