<template>
  <div class="bigcontent">
    <el-button type="info" @click="logout"> 退出 </el-button>
    <el-container>
      <el-header>Header</el-header>
      <el-container>
        <el-aside width="200px">Aside</el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  methods: {
    logout () {
      window.sessionStorage.clear()
      this.$router.push('/login')
    }
  }
}
</script>

<style lang='less' scoped>
.bigcontent{
 height: 100%;
}
.el-container{
  height: 100%;
  .el-header{
    background: #373D41;
  }
  .el-aside{
    background: #373D41;
  }
}
</style>
