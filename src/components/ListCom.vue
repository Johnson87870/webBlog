<template>
  <div class="list">
    <div class="list-item">
      <div class="list-item-left">
        <div class="list-title">推荐一些实用的Mac工具</div>
        <div class="list-content">
          今天，美团是中国市值第三的互联网公司，技术团队也已经达到9000多人规模，覆盖前端、后台、系统、算法、测试、运维、数据、硬件等8个技术领域。
          2013年美团公司年会上，王兴特别引用了清华大学老校长梅贻琦先生的一句名言：“大学者，非谓有大楼之谓也，有大师之谓也。”他是告诉在场的美团同学：选择跟什么样的人在一起做什么样的事，很重要。
          最近，美团技术学院陆续采访了20多位美团技术团队的同学，既有美团早期创始团队的3位“元老”，也有很多美团App、美团外卖等部门的技术骨干，听他们聊了聊自己跟公司一起成长的故事。故事里有争吵，也有友情；有汗水，也有泪水；有委屈，也有成长；有迷茫，也有坚定。我们从中摘录了他们印象最深刻的一些片段，与大家一起感受，10年来美团技术团队经历的那些坎坷与崎岖，收获的那些感动和期许。
          作者：美团技术团队
          链接：https://juejin.im/post/5e61f4d2e51d4526c80eaaa9
          来源：掘金
          著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
        </div>
        <div class="list-other">
          <button class="viewed">
            <span class="icon"></span>
            <span class="text">99+</span>
          </button>
          <button class="like">
            <span class="icon"></span>
            <span class="text">99+</span>
          </button>
          <button class="no_like">
            <span class="icon"></span>
            <span class="text">0</span>
          </button>
        </div>
      </div>
      <div class="list-item-right">
        <img src="../assets/imgs/userpt.png" alt />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.list {
  width: 100%;
  overflow: hidden;
  > .list-item {
    height: 100px;
    overflow: hidden;
    display: flex;
    margin: 10px;
    padding: 5px;
    border-bottom: 1px solid #ccc;
    > .list-item-left {
      flex: 1;
      padding-right: 10px;
      color: #342648;
      > .list-title {
        font-size: 20px;
        font-weight: bold;
      }
      > .list-content {
        padding-top: 4px;
        overflow: hidden;
        font-size: 14px;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 2;
      }
      > .list-other {
        display: flex;
        padding-top: 4px;
        font-size: 14px;
        > button {
          width: 80px;
          height: 25px;
          margin: 0 12px;
          padding: 0 10px;
          display: flex;
          align-items: center;
          justify-content: space-between;
          background-color: #fff;
          color: #0094ff;
          font-weight: bold;
          border-radius: 40px;
          border: 2px solid #0094ff;
        }
        > button:first-child {
          margin-left: 0;
        }
        .icon {
          width: 20px;
          height: 20px;
          background-size: 100% 100% !important;
          background-repeat: no-repeat !important;
        }
        > .viewed {
          > .icon {
            background: url("../assets/icons/browse.png");
          }
        }
        > .like {
          > .icon {
            background: url("../assets/icons/Like.png");
          }
        }
        > .no_like {
          > .icon {
            background: url("../assets/icons/Dislike.png");
          }
        }
      }
    }
    > .list-item-right {
      width: 80px;
      height: 100%;
      > img {
        width: 100%;
        height: 100%;
      }
    }
  }
}
</style>