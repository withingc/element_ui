<template>
  <div id="app">

    <el-row type="flex" id="navigate">
      <el-col :span="2"><div class="grid-content"><img src="./assets/assassin.jpg" height="60"></div></el-col>
      <el-col :span="8"><div class="grid-content" style="height: 50px">
        <div style="height: 30px;margin: 10px" >WITHING</div>
      </div></el-col>
      <el-col :span="10"><div class="grid-content">
        <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect" active-text-color="#00BFFF">
          <el-menu-item index="1">withing的主页</el-menu-item>
          <el-menu-item index="2">Games pictures</el-menu-item>
          <el-menu-item index="3">Favorite</el-menu-item>
        </el-menu>
      </div></el-col>
      <el-col :span="4"><div>
        <el-input placeholder="请输入内容" v-model="input10" clearable>
        </el-input>
      </div></el-col>
    </el-row>
    <el-row><div style="height: 30px"></div></el-row>
    <el-row id="carousel">
      <el-col :span="6">h</el-col>
      <el-col :span="12"><div class="block">
        <el-carousel height="300px">
          <el-carousel-item v-for="item in 4" :key="item">
            <h3>{{ item }}</h3>
          </el-carousel-item>
        </el-carousel>
      </div></el-col>
      <el-col :span="6">h</el-col>
    </el-row>
  </div>

</template>

<script>
export default {
    data() {
        return {
            input10: ''
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

  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
</style>