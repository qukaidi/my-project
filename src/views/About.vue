<template>
  <div class="about">
    <van-nav-bar left-text="微信" :fixed="true">
      <van-icon name="search" slot="right" />
      <van-icon name="add-o" slot="right" />
    </van-nav-bar>
    <van-pull-refresh v-model="refreshing" @refresh="onRefresh">
      <van-list v-model="loading" :finished="finished" finished-text="没有更多了" @load="onLoad">
        <van-cell v-for="item in list" :key="item">
          <div class="ac">
            <img width="50" height="50" src="../assets/tx.jpg" />
            <div>
              <span class="custom-title">昵称</span><br>
              <span class="custom-text">消息内容</span>
            </div>
          </div>
        </van-cell>
      </van-list>
    </van-pull-refresh>
  </div>
</template>
<script>
export default {
  data() {
    return {
      list: [],
      loading: false,
      finished: false,
      refreshing: false
    };
  },
  methods: {
    onLoad() {
      setTimeout(() => {
        if (this.refreshing) {
          this.list = [];
          this.refreshing = false;
        }

        for (let i = 0; i < 10; i++) {
          this.list.push(this.list.length + 1);
        }
        this.loading = false;

        if (this.list.length >= 40) {
          this.finished = true;
        }
      }, 1000);
    },
    onRefresh() {
      // 清空列表数据
      this.finished = false;

      // 重新加载数据
      // 将 loading 设置为 true，表示处于加载状态
      this.loading = true;
      this.onLoad();
    }
  }
};
</script>
<style lang="less">
.about {
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
  .ac {
    display: flex;
    align-items: center;
    img{
      border-radius: 5px;
    }
    div{
      margin-left: 5px;
      .custom-text{
        color: #a8a8a8;
        font-size: 12px
      }
    }
  }
}
</style>