<template>
  <div id="app">
    <router-view class="mt-mb"/>
    <van-tabbar v-model="active" active-color="#07c160" inactive-color="#000">
      <van-tabbar-item name="wx" icon="home-o" info="5" to="/About">微信</van-tabbar-item>
      <van-tabbar-item name="addressBook" icon="search" to="/AddressBook">通讯录</van-tabbar-item>
      <van-tabbar-item name="find" icon="friends-o">发现</van-tabbar-item>
      <van-tabbar-item name="me" icon="setting-o">我</van-tabbar-item>
    </van-tabbar>
  </div>
</template>
<script>
export default {
  name: "home",
  data() {
    return {
      active: "wx"
    };
  }
};
</script>
<style lang="less">
.mt-mb{
  margin-top: 46px;
  margin-bottom: 46px;
}
</style>
