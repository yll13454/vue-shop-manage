<template>
  <div class="main_cantainer">
    <el-container>
      <el-header>
        <div class="headleft">
          <img src="../assets/logo.png" alt="" srcset="" />
          <span>商城后台管理系统</span>
        </div>
        <el-button @click="logout">退出</el-button>
      </el-header>
      <el-container>
        <el-aside width="200px">
          <el-menu
            class="el-menu-vertical-demo"
            background-color="#333744"
            text-color="#fff"
            active-text-color="#409FFF"
          >
            <el-submenu index="1">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span>导航一</span>
              </template>
              <el-menu-item index="1-1">选项1</el-menu-item>
            </el-submenu>
          </el-menu>
        </el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  methods: {
    logout() {
      window.sessionStorage.clear()
      this.$router.push('/login')
    }
  }
}
</script>

<style lang="scss" scoped>
.main_cantainer {
  height: 100%;
}
.el-header {
  background-color: rgb(51, 58, 60);
  color: #333;
  text-align: center;
  line-height: 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .headleft {
    display: flex;
    justify-content: center;
    align-items: center;
    img {
      height: 50px;
      width: 50px;
    }
    span {
      color: white;
      margin-left: 24px;
    }
  }
}
.el-button {
  background-color: white;
  height: 42px;
}
.el-aside {
  background-color: rgb(47, 52, 64);
  color: #fff;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

.el-container {
  height: 100%;
  color: #fff;
}
</style>
