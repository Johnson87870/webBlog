<template>
  <div class="menus">
    <div class="card">
      <div class="card-head-image">
        <img src="../assets/imgs/userpt.png" alt />
      </div>
      <div class="card-head-intro">
        <div class="card-mine-name">Johnson</div>
        <div class="card-mind-job">WEB前端开发</div>
        <div class="card-mind-sign">
          <span class="sign-label">签名:</span>
          <span class="sign-value">一路逆风!!!</span>
        </div>
      </div>
    </div>
    <div class="menus-nav">
      <a href="#" class="nav-item" @click="goToRoutePage('/')">
        <span class="nav-icon">
          <img src="../assets/icons/home.svg" alt />
        </span>
        <span class="nav-text">
          首页
          <!-- <router-link to="/">首页</router-link> -->
        </span>
      </a>
      <a href="#" class="nav-item" @click="goToRoutePage('bloglist')">
        <span class="nav-icon">
          <img src="../assets/icons/bloglist.svg" alt />
        </span>
        <span class="nav-text">
          博客文章
          <!-- <router-link to="/bloglist">博客文章</router-link> -->
        </span>
      </a>
      <a href="#" class="nav-item" @click="goToRoutePage('document')">
        <span class="nav-icon">
          <img src="../assets/icons/document.svg" alt />
        </span>
        <span class="nav-text">
          文档
          <!-- <router-link to="/document">文档</router-link> -->
        </span>
      </a>
      <a href="#" class="nav-item" @click="goToRoutePage('about')">
        <span class="nav-icon">
          <img src="../assets/icons/about.svg" alt />
        </span>
        <span class="nav-text">
          关于
          <!-- <router-link to="/about">关于</router-link> -->
        </span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    // 路由跳转
    goToRoutePage(type) {
      const routerType = type.indexOf("/") == -1 ? "/" + type : type;
      this.$router.push({ path: routerType });
    }
  }
};
</script>

<style lang="scss" scoped>
.menus {
  width: 180px;
  overflow: hidden;
  > .card {
    width: 100%;
    padding-top: 15px;
    padding-bottom: 15px;
    // #fff1ed, #ebedee
    background: linear-gradient(80deg, #e6e9f0, #eef1f5);
    box-shadow: 0 1px 3px 0 #f5f5f5;
    position: relative;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    // filter: blur(1px);
    > .card-head-image {
      float: left;
      margin-left: 5px;
      width: 50px;
      height: 50px;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      border-radius: 50%;
      border: 1px #ccc solid;
      > img {
        width: 100%;
        height: 100%;
        border-radius: 50%;
        transform: rotate(1turn);
        transition-duration: 1.5s;
        transition-timing-function: cubic-bezier(0.34, 0, 0.84, 1);
      }
      > img:hover {
        transform: rotate(666turn);
        transition-duration: 59s;
        transition-timing-function: cubic-bezier(0.34, 0, 0.84, 1);
      }
    }
    > .card-head-intro {
      padding: 8px 5px 8px 65px;
      font-size: 14px;
      color: #342648;
      > .card-mine-name {
        font-size: 18px;
        font-weight: bold;
      }
      > .card-mind-job {
        font-size: 16px;
      }
      > .card-mind-sign {
      }
    }
  }
  > .menus-nav {
    padding-top: 10px;
    height: 80vh;
    background: linear-gradient(#8895b1, #bcc2d7);
    border-bottom-right-radius: 5px;
    border-bottom-left-radius: 5px;
    > .nav-item {
      height: 50px;
      border-bottom: 1px #ccc solid;
      display: flex;
      align-items: center;
      text-decoration: none;
      color: #342648;
      > .nav-icon {
        width: 40px;
        height: 40px;
        margin-left: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        > img {
          height: 30px;
          width: 40px;
        }
      }
      > .nav-text {
        width: 50%;
        margin-left: 20px;
        text-align: start;
      }
    }
    > .nav-item:last-child {
      border: 0;
    }
    > .nav-item:hover {
      color: #fff;
    }
    > .nav-item:active {
      color: #fff;
    }
  }
}
</style>