<template>
  <div id="app">

    <el-row type="flex">
      <el-col :span="2"><div class="grid-content"><img src="./assets/assassin.jpg" height="60"></div></el-col>
      <el-col :span="12"><div class="grid-content">
        <div class="">WITHING</div>
      </div></el-col>
      <el-col :span="10"><div class="grid-content">
        <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect" active-text-color="#00BFFF">
          <el-menu-item index="1">withing的主页</el-menu-item>
          <el-menu-item index="2">Games pictures</el-menu-item>
          <el-menu-item index="3">Favorite</el-menu-item>
        </el-menu>
      </div></el-col>
    </el-row>
  </div>

</template>

<script>
export default {
  methods: {
    startHacking () {
      this.$notify({
        title: 'It works!',
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000
      })
    }
  }
}
</script>

<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
</style>
<style>
  .el-row {
    margin-bottom: 20px;
  &:last-child {
     margin-bottom: 0;
   }
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
</style>