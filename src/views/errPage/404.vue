<template>
  <div class="wscn-http404-container">
    <div class="wscn-http404">
      <div class="pic-404">
        <!-- <img class="pic-404__parent" src="@/assets/404_images/404.png" alt="404"> -->
      </div>
      <div class="bullshit">
        <div class="bullshit__oops">Page not found!</div>
        <!-- <div class="bullshit__info">
          版权所有
          <a class="link-type" href="https://wallstreetcn.com" target="_blank">华尔街见闻</a>
        </div>-->
        <div class="bullshit__headline">{{ message }}</div>
        <div class="bullshit__info">请检查您输入的网址是否正确</div>
        <router-link to="/" class="bullshit__return-home">返回首页</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page404",
  computed: {
    message() {
      return "输入的网址有误";
    }
  }
};
</script>

<style scoped>
.wscn-http404-container {
  transform: translate(-50%, -50%);
  position: absolute;
  top: 40%;
  left: 50%;
}
.wscn-http404 {
  position: relative;
  width: 1200px;
  padding: 0 50px;
  overflow: hidden;
}

.pic-404 {
  position: relative;
  float: left;
  width: 500px;
  overflow: hidden;
}
.pic-404__parent {
  width: 100%;
  height: 100%;
}
.pic-404__child {
  position: absolute;
}

.bullshit {
  position: relative;
  float: left;
  top: 20px;
  width: 300px;
  padding: 30px 0;
  overflow: hidden;
}

.bullshit__oops {
  font-size: 32px;
  font-weight: bold;
  line-height: 40px;
  color: #1482f0;
  opacity: 0;
  margin-bottom: 20px;
  animation-name: slideUp;
  animation-duration: 0.5s;
  animation-fill-mode: forwards;
}
.bullshit__headline {
  font-size: 20px;
  line-height: 24px;
  color: #222;
  font-weight: bold;
  opacity: 0;
  margin-bottom: 10px;
  animation-name: slideUp;
  animation-duration: 0.5s;
  animation-delay: 0.1s;
  animation-fill-mode: forwards;
}
/* .bullshit__info {
  font-size: 13px;
  line-height: 21px;
  color: grey;
  opacity: 0;
  margin-bottom: 30px;
  animation-name: slideUp;
  animation-duration: 0.5s;
  animation-delay: 0.2s;
  animation-fill-mode: forwards;
} */
.bullshit__return-home {
  display: block;
  margin-top: 20px;
  float: left;
  width: 110px;
  height: 36px;
  background: #1482f0;
  border-radius: 100px;
  text-align: center;
  color: #ffffff;
  opacity: 0;
  font-size: 14px;
  line-height: 36px;
  cursor: pointer;
  animation-name: slideUp;
  animation-duration: 0.5s;
  animation-delay: 0.3s;
  animation-fill-mode: forwards;
}
@keyframes slideUp {
  0% {
    transform: translateY(60px);
    opacity: 0;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}
</style>
