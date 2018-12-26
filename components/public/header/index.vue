<template>
  <el-row
    :gutter="0"
    class="m-header"
  >
    <el-col :span="4">
      <Geo/>
    </el-col>
    <el-col :span="6">
      <User/>
    </el-col>
    <el-col :span="14">3</el-col>
  </el-row>
</template>

<script>
import Geo from './geo'
import User from './user'
export default {
  components: {
    Geo,
    User
  }
}
</script>

<style lang="scss">
@import '@/assets/css/public/layout.scss';
</style>
