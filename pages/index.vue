<template>
  <div>
    <el-card class="mt-20 tracking_container">
      <div>
        <div class="">
          <h4>Tracking ID:</h4>
          <p></p>
        </div>
        <div class="">
          <h4>Statement Date:</h4>
          <p></p>
        </div>
        <div class="">
          <h4>Goods/Items Tracking:</h4>
          <p></p>
        </div>
        <div class="">
          <h4>Quantity:</h4>
          <p></p>
        </div>
        <div class="">
          <h4>Delivery Date :</h4>
          <p></p>
        </div>
      </div>
    </el-card>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage',
  data() {
    return {}
  },
  methods: {},
})
</script>

<style lang="scss" scoped>
$small_screen: 426px;
$medium_screen: 769px;
$laptop_screen: 1024px;
.tracking_container {
  padding: 20px;
  min-height: 500px;
}
</style>
