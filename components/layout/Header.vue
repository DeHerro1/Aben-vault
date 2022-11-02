<template>
  <div class="dashboard-header d-flex justify_between">
    <h3 class="page__title">{{ pageTitle }}</h3>
    <div class="d-flex">
      <el-dropdown trigger="click">
        <span class="dashboard-header__user">
          <el-avatar
            size="large"
            src="https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png"
          ></el-avatar>
          <div class="ml-10">
            <span class="text-black">
              <!-- {{ $auth.user.first_name }} {{ $auth.user.last_name }} -->
            </span>
            <br />
            <small>Admin User</small>
          </div>

          <i class="el-icon-arrow-down"></i>
        </span>
        <el-dropdown-menu slot="dropdown">
          <div class="dashboard-dropdown">
            <ul>
              <li>
                <i class="el-icon-user"></i>
                <span> Account </span>
              </li>
              <hr class="hr_rule" />
              <li class="mt-5">
                <i class="el-icon-setting"></i>
                <span> Logout </span>
              </li>
            </ul>
          </div>
        </el-dropdown-menu>
      </el-dropdown>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'HeaderPage',
  data() {
    return {
      pageTitle: '' as string,
      notify_count: 0,
    }
  },
  watch: {
    $route(to) {
      this.setRoutesNames(to.name)
    },
  },
  created() {
    this.setRoutesNames(this.$route.name!)
  },
  methods: {
    setRoutesNames(routeName: string) {
      this.pageTitle =
        routeName === 'index'
          ? 'Tracking Status'
          : routeName === 'customer-information'
          ? 'Customer Information'
          : routeName === 'manage-password'
          ? 'Manage Password'
          : routeName
    },
    // async logout() {
    //   await this.$auth.logout()
    //   this.$router.push({
    //     name: 'Login',
    //   })
    // },
  },
})
</script>

<style lang="scss" scoped>
.dashboard-header {
  width: 100%;
  padding: 20px;
  align-items: center;

  .page__title {
    flex-basis: 100%;
  }
}
</style>
