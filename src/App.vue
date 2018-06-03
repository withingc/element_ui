<template>
  <div id="app">

    <el-row>
      <el-col :span="8"><div class="grid-content bg-purple">哈哈哈哈哈哈哈哈</div></el-col>
      <el-col :span="8"><div class="grid-content bg-purple-light">
        <img src="./assets/logo.png">
        <div>
          <el-button @click="startHacking">Start</el-button>
        </div>
      </div></el-col>
      <el-col :span="8"><div class="grid-content bg-purple">哈哈哈哈哈哈哈哈</div></el-col>
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
