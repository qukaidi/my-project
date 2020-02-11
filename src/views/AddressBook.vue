<template>
  <div class="addressbook">
    <van-nav-bar left-text="通讯录" :fixed="true">
      <van-icon name="search" slot="right" />
      <van-icon name="add-o" slot="right" />
    </van-nav-bar>
    <div class="mt">
      <van-index-bar :index-list="indexList" :sticky-offset-top="46">
         <van-index-anchor index="A">A</van-index-anchor>
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-index-anchor index="B">B</van-index-anchor>
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-index-anchor index="C">C</van-index-anchor>
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-index-anchor index="D">D</van-index-anchor>
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-index-anchor index="E">E</van-index-anchor>
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-index-anchor index="F">F</van-index-anchor>
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-index-anchor index="G">G</van-index-anchor>
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
        <van-cell title="文本" />
      </van-index-bar>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      indexList: ["A", "B", "C", "D", "E", "F", "G"]
    };
  }
};
</script>
<style lang="less">
.addressbook {
  .van-nav-bar {
    background-color: #f5f5f6;
    z-index: 2 !important;
    .van-nav-bar__text {
      color: #000;
    }
    .van-icon {
      color: #000;
      margin-left: 15px;
    }
    .van-nav-bar__left {
      font-size: 16px;
    }
    .van-nav-bar__right {
      font-size: 18px;
    }
  }
  .mt {
    margin-top: 46px;
  }
}
</style>