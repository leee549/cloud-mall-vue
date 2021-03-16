<template>
  <!-- <transition name="fade" mode="out-in"> -->
    <router-view></router-view>
  <!-- </transition> -->
</template>

<script>
  export default {
    computed: {
        key() {
          return this.$route.path
        }
      }
  }
</script>
<style lang="less">
  /* 解决element-ui的table表格控件表头与内容列不对齐问题 */
  .el-table th.gutter{
    display: table-cell!important;
  }
  .el-table__row{
  td:not(.is-hidden):last-child{
    right:-1px;
  }}

// .fade-enter {
//  opacity:0;
// }
// .fade-leave{
//  opacity:1;
// }
// .fade-enter-active{
//  transition:opacity .5s;
// }
// .fade-leave-active{
//  opacity:0;
//  transition:opacity .5s;
// }
</style>
