<template>
  <el-aside>
    <div>
      <div class="sidebar_logo_div">
        <!-- <img src="../../assets/img/logo.png" alt="logo" width="100px" /> -->
      </div>
      <br />
      <el-menu :default-openeds="['1']" router active-text-color="black">
        <el-menu-item index="1" :route="{ path: '/' }">
          <i class="el-icon-s-marketing"></i>
          Tracking Status</el-menu-item
        >
        <el-menu-item index="2" :route="{ path: '/customer-information' }">
          <i class="el-icon-shopping-cart-full"></i>
          Customer information</el-menu-item
        >
        <el-menu-item index="3" :route="{ path: '/manage-password' }">
          <i class="el-icon-goods mr-5"></i>
          Manage Password
        </el-menu-item>
        <el-menu-item index="4" :route="{ path: '/users' }">
          <i class="el-icon-user-solid mr-5"></i>
          Logout
        </el-menu-item>
      </el-menu>
    </div>

    <!-- <div>
      <el-menu router active-text-color="rgb(229, 221, 241);">
        <el-menu-item index="6" :route="{ path: '/' }">
          <i class="el-icon-setting"></i>
          Settings</el-menu-item
        >
        <el-menu-item index="7" :route="{ path: '/schedules' }">
          <i class="el-icon-help"></i>
          Help</el-menu-item
        >
      </el-menu>
    </div> -->
  </el-aside>
</template>

<script>
export default {
  name: 'SidebarPage',
}
</script>

<style lang="scss" scoped>
.el-aside {
  width: 250px !important;
  height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: margin 0.6s ease-in-out 0s;

  .sidebar_logo_div {
    box-shadow: 0 2px 10px rgb(0 0 0 / 8%);
    padding: 15px 15px 13px 15px;
    padding-left: 30px;
    padding-top: 20px;
    background-color: #fff;
    height: 68px;
  }
}

.el-menu {
  background-color: transparent;
}
</style>
