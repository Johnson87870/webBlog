<template>
  <div class="welcome">
    <div class="welcome-filter">
      <div class="welcome-head-image">
        <img src="../assets/imgs/userpt.png" alt />
      </div>
      <div class="welcome-sign">Johnson</div>
      <div class="welcome-intro">
        <p>欢迎你查看我的博客,这里面记录我一些开发的笔记文档,还有一些技术框架的技术教程...</p>
        <p>欢迎大家一起探讨!!!</p>
      </div>
    </div>

    <div class="welcome-sign-in">
      <button class="welcome-sign-in-button" @click="$router.push({ path: '/home' })">
        <span class="welcome-sign-start-btn">Start !</span>
        <span class="welcome-sign-enter-btn">Enter my blog !</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    EnterIn() {
      this.$router.push({ path: "/" });
    }
  }
};
</script>

<style lang="scss" scoped>
.welcome {
  width: 100vw;
  height: 100vh;
  display: flex;
  position: fixed;
  left: 0;
  top: 0;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-image: url("../assets/imgs/welcomeBg.png");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  color: #fff;

  > .welcome-filter {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 20px 0;
    z-index: 1;
    position: relative;
    overflow: hidden;
    background-position: center top;
    background-size: cover;
    > .welcome-head-image {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      border: 10px #fff solid;
      box-shadow: 0 0 20px 0 #cccccc;
      > img {
        width: 100%;
        height: 100%;
        border-radius: 50%;
      }
    }
    > .welcome-sign {
      padding-top: 20px;
      font-size: 24px;
      font-weight: bold;
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    }
  }

  > .welcome-filter::after {
    clear: both;
    content: "";
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: -1;
    background-image: url("../assets/imgs/welcomeBg.png");
    background-position: center top;
    background-size: cover;
    background-attachment: fixed;
    -webkit-filter: blur(20px);
    -moz-filter: blur(20px);
    -ms-filter: blur(20px);
    -o-filter: blur(20px);
    filter: blur(20px);
  }

  > .welcome-sign-in {
    margin-top: 20px;
    width: 200px;
    display: flex;
    justify-content: center;
    > .welcome-sign-in-button {
      width: 60px;
      height: 50px;
      font-size: 16px;
      border-radius: 40px;
      background-color: #fff;
      color: #342648;
      font-weight: bold;
      border: 0;
      position: relative;
      > span {
        position: absolute;
        left: 0;
        top: 0;
        display: flex;
        width: 100%;
        height: 100%;
        justify-content: center;
        align-items: center;
      }
      > .welcome-sign-start-btn {
        opacity: 1;
      }
      > .welcome-sign-enter-btn {
        opacity: 0;
      }
    }
  }

  > .welcome-sign-in:hover {
    > .welcome-sign-in-button {
      width: 200px;
      height: 50px;
      border-radius: 40px;
      background-color: #0094ff;
      transition-duration: 0.8s;
      transition-timing-function: ease;

      > span {
        display: flex;
        width: 100%;
        height: 100%;
        justify-content: center;
        align-items: center;
      }
      > .welcome-sign-start-btn {
        animation: text-out 0.4s ease;
        -moz-animation: text-out 0.4s ease;
        -webkit-animation: text-out 0.4s ease;
        animation-fill-mode: both;
      }
      > .welcome-sign-enter-btn {
        color: #fff;
        animation: text-in 0.4s ease 0.15s;
        -moz-animation: text-in 0.4s ease 0.15s;
        -webkit-animation: text-in 0.4s ease 0.15s ease;
        animation-fill-mode: both;
      }
    }
  }
}

@keyframes text-out {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
@-moz-keyframes text-out {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
@-webkit-keyframes text-out {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}

@keyframes text-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@-webkit-keyframes text-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@-moz-keyframes text-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>