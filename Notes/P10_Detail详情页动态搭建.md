步骤：创建对应的vue、json、js文件后

在app.json添加页面



编写detail.vue

```vue
<template>
  <div>
    <div class="detailContainer">
      <img class="detail_img" src="/static/images/index/cart.jpg" alt="">

      <div class="avatar_date">
        <img src="/static/images/avatar/0.png" alt="">
        <span>新华社</span>
        <span>发布于</span>
        <span>2018</span>
      </div>
      <p class="company">贾静雯简介</p>
      <div class="collection_share_container">
        <div class="collection_share">
          <img @tap="handleCollection" src="/static/images/icon/collection-anti.png" alt="">
          <img @tap="handleShare" src="/static/images/icon/share-anti.png" alt="">
        </div>
        <div class="line"></div>
      </div>
      <Button open-type="share">转发此文章</Button>
      <p class="content">贾静雯是我女神</p>
    </div>
    </div></div>
  </div>
</template>
<script>
  export default {
  }
</script>
<style>
  .detailContainer {
    display: flex;
    flex-direction: column;
  }

  .detail_img {
    width: 100%;
    height: 460rpx;
  }
  .avatar_date{
    padding:10rpx;
  }
  .avatar_date img {
    width: 64rpx;
    height: 64rpx;
    vertical-align: middle;
  }

  .avatar_date span {
    font-weight: 28rpx;
    margin-left: 6rpx;
  }

  .company {
    font-size: 32rpx;
    font-weight: bold;
    padding:10rpx;
  }

  .collection_share_container {
    position: relative;
  }

  .collection_share {
    float: right;
    margin-right: 30rpx;
  }

  .collection_share img {
    width: 90rpx;
    height: 90rpx;
    margin-right: 20rpx;
  }

  .line {
    position: absolute;
    top: 45rpx;
    left: 5%;
    width: 90%;
    height:1rpx;
    background: #eee;
    z-index: -1;
  }

  .content {
    font-size: 32rpx;
    text-indent: 32rpx;
    letter-spacing: 3rpx;
    line-height: 50rpx;
  }

  .music_img {
    width: 60rpx;
    height: 60rpx;
    position: absolute;
    top: 200rpx;
    left: 50%;
    margin-left: -30rpx;
  }
</style>
```