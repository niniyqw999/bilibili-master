<template>
  <div>
    <div class="header">
      <div class="header-nav">
        <div class="menu">
          <ul>
            <li>
              <span class="iconfont icon-bilibili icon1 icon3"></span>
              <span style="position: relative; bottom: 3.5px">首页</span>
            </li>
            <li><span>番剧</span></li>
            <li @mouseenter="live = true" @mouseleave="live = false">
              <span>直播</span>
            </li>
            <li @mouseenter="game = true" @mouseleave="game = false">
              <span>游戏中心</span>
            </li>
            <li><span>会员购</span></li>
            <li @mouseenter="book = true" @mouseleave="book = false">
              <span>漫画</span>
            </li>
            <li><span>赛事</span></li>
            <li @mouseenter="download = true" @mouseleave="download = false">
              <span class="iconfont icon-download-1-copy icon2 icon3"></span>
              <span>下载客户端</span>
            </li>
          </ul>
        </div>
        <div class="search">
          <input
            type="text"
            placeholder="搜索"
            @focus="searchFoucs"
            @blur="searchBlur"
          />
          <span class="iconfont icon-fangdajing icon1"></span>
          <div class="shDialog" v-if="searchDialog">
            <ul>
              <h2 style="font-size: 18px">搜索历史</h2>
              <h3 style="font-size: 10px; color: #61666d">清空</h3>
            </ul>
            <ul>
              <li>前端开发</li>
              <li>JavaScript进阶</li>
              <li>怎么学习前端</li>
              <li>css布局</li>
              <li>vue框架</li>
              <li>vue2和vue3</li>
            </ul>
            <ol>
              <h2>bilibili热搜</h2>
              <li>BLG全球冠军赛首胜</li>
              <li>G2喊话theshy</li>
              <li>uzi哭了</li>
              <li>wbg战胜edg</li>
              <li>xxxxx</li>
              <li>xxxxxxx</li>
              <li>xxxxxx</li>
              <li>xxxxx</li>
              <li>xxxxxx</li>
              <li>xxxxxxx</li>
            </ol>
          </div>
        </div>
        <div class="user">
          <ul>
            <li
              class="user-img"
              @mouseenter="userDialog = true"
              @mouseleave="userDialog = false"
            >
              <img src="../assets/img/user.jpg" alt="" />
              <div class="user-content" v-if="userDialog">
                <h2 style="margin-top: 50px">工藤新一</h2>
                <ul style="font-size: 12px; color: #85888a; margin-top: 5px">
                  <li>硬币:999</li>
                  <li>B币:999</li>
                </ul>
                <ul style="margin: 10px 0px">
                  <li
                    style="
                      color: white;
                      text-shadow: -1px -1px 0 skyblue, 1px -1px 0 skyblue,
                        -1px 1px 0 skyblue, 1px 1px 0 skyblue;
                    "
                  >
                    lv3
                  </li>
                  <li
                    style="
                      width: 180px;
                      height: 2px;
                      background: linear-gradient(
                        to right,
                        orange 50%,
                        #cad0d4 50%
                      );
                    "
                  ></li>
                  <li
                    style="
                      color: white;
                      text-shadow: -1px -1px 0 #cad0d4, 1px -1px 0 #cad0d4,
                        -1px 1px 0 #cad0d4, 1px 1px 0 #cad0d4;
                    "
                  >
                    lv4
                  </li>
                </ul>
                <span style="font-size: 12px; color: #d0d3d6"
                  >当前成长2500,距离升级lv.4还需要成长2500</span
                >
                <ul style="margin: 10px 0">
                  <li
                    style="
                      display: flex;
                      flex-direction: column;
                      margin-right: 40px;
                    "
                  >
                    <span>999</span>
                    <span style="font-size: 12px; color: #b4b7bb">关注</span>
                  </li>
                  <li
                    style="
                      display: flex;
                      flex-direction: column;
                      margin-right: 40px;
                    "
                  >
                    <span>999</span>
                    <span style="font-size: 12px; color: #b4b7bb">粉丝</span>
                  </li>
                  <li style="display: flex; flex-direction: column">
                    <span>999</span>
                    <span style="font-size: 12px; color: #b4b7bb">动态</span>
                  </li>
                </ul>
                <div
                  style="
                    width: 260px;
                    height: 60px;
                    background: rgb(254, 223, 228);
                    margin: 15px 20px;
                    position: relative;
                    border-radius: 5px;
                    border: 0;
                  "
                >
                  <span
                    style="
                      color: rgb(239, 97, 189);
                      position: absolute;
                      top: 15px;
                      left: 10px;
                      font-size: 14px;
                    "
                    >大会员×QQSVIP特惠中</span
                  >
                  <span
                    style="
                      font-size: 12px;
                      color: #616161;
                      position: absolute;
                      top: 35px;
                      left: 10px;
                    "
                    >168元买一年送一年</span
                  >
                  <button
                    style="
                      position: absolute;
                      top: 17px;
                      left: 170px;
                      width: 70px;
                      height: 27px;
                      font-size: 12px;
                      background: white;
                      border-radius: 5px;
                      border: 0;
                      color: rgb(240, 157, 171);
                    "
                  >
                    立即开通
                  </button>
                </div>
                <ul
                  style="
                    font-size: 14px;
                    color: #616161;
                    display: flex;
                    flex-direction: column;
                    position: relative;
                    left: -90px;
                  "
                >
                  <li style="margin-bottom: 30px">个人中心</li>
                  <li style="margin-bottom: 30px">投稿管理</li>
                  <li style="margin-bottom: 30px">推荐服务</li>
                  <li>退出登录</li>
                </ul>
              </div>
            </li>
            <li>
              <span class="iconfont icon-31huiyuan icon1"></span>
            </li>
            <li>
              <span class="iconfont icon-youjian icon1"></span>
            </li>
            <li>
              <span class="iconfont icon-fengche icon1"></span>
            </li>
            <li>
              <span class="iconfont icon-31shoucang icon1"></span>
            </li>
            <li>
              <span class="iconfont icon-lishixiao icon2"></span>
            </li>
            <li>
              <span class="iconfont icon-bulb icon2"></span>
            </li>
            <li class="user-upload">
              <span class="iconfont icon-shangchuan icon2"></span>
            </li>
          </ul>
        </div>
      </div>
      <div class="logo"></div>
      <div
        class="live"
        v-if="live"
        @mouseenter="live = true"
        @mouseleave="live = false"
      >
        <div class="live-left">
          <h1>热门直播</h1>
          <img src="../assets/img/user.jpg" alt="" />
          <img src="../assets/img/user.jpg" alt="" />
          <img src="../assets/img/user.jpg" alt="" />
          <img src="../assets/img/user.jpg" alt="" />
          <img src="../assets/img/user.jpg" alt="" />
          <img src="../assets/img/user.jpg" alt="" />
        </div>
        <div class="live-right">
          <h1>热门活动</h1>
          <img src="" alt="" />
          <img src="" alt="" />
        </div>
      </div>
      <div
        class="game"
        v-if="game"
        @mouseenter="game = true"
        @mouseleave="game = false"
      >
        <div class="game-left">
          <img src="" alt="" />
          <img src="" alt="" />
          <img src="" alt="" />
          <img src="" alt="" />
        </div>
        <div class="game-right">
          <h2>新游预告</h2>
          <ul>
            <li>英雄联盟</li>
            <li>lol</li>
            <li>穿越火线</li>
            <li>cf</li>
            <li>地下城勇士</li>
            <li>dnf</li>
            <li>QQ</li>
          </ul>
        </div>
      </div>
      <div
        class="book"
        v-if="book"
        @mouseenter="book = true"
        @mouseleave="book = false"
      >
        <div class="book-left">
          <img src="" alt="" />
          <img src="" alt="" />
          <img src="" alt="" />
          <img src="" alt="" />
        </div>
        <div class="book-right">
          <h2>人气漫画</h2>
          <ol>
            <li>七龙珠</li>
            <li>海贼王</li>
            <li>名侦探柯南</li>
            <li>名侦探柯南</li>
            <li>名侦探柯南</li>
            <li>名侦探柯南</li>
          </ol>
        </div>
      </div>
      <div
        class="download"
        v-if="download"
        @mouseenter="download = true"
        @mouseleave="download = false"
      >
        <div class="down-left">
          <ul>
            <li><span>手机版</span></li>
            <li><span>扫码即可下载手机app</span></li>
            <li>
              <img src="" alt="" />
            </li>
          </ul>
        </div>
        <div class="down-right">
          <ul>
            <li><span>电脑windows版</span></li>
            <li>适合win系统设备</li>
            <li>
              <img src="" alt="" />
            </li>
            <li>
              <button>立即下载</button>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="category">
      <div class="total">
        <div class="left">
          <ul>
            <li>
              <svg class="icon" aria-hidden="true">
                <use xlink:href="#icon-huoreremen"></use>
              </svg>
              <span>动态</span>
            </li>
            <li>
              <svg class="icon" aria-hidden="true">
                <use xlink:href="#icon-huoreremen"></use>
              </svg>
              <span>热门</span>
            </li>
            <li>
              <svg class="icon" aria-hidden="true">
                <use xlink:href="#icon-ziyuan"></use>
              </svg>
              <span>频道</span>
            </li>
          </ul>
        </div>
        <div class="center">
          <ul>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li><span>xxx</span></li>
            <li>
              <span>更多</span>
              <span class="iconfont icon-xiangxiajiantou"></span>
            </li>
          </ul>
        </div>
      </div>
      <el-divider direction="vertical" style="height: 60%; z-index: -1" />
      <div class="right">
        <ul>
          <li>
            <span class="iconfont icon-zhuanlan"></span>
            <span>专栏</span>
          </li>
          <li>
            <span class="iconfont icon-zhuanlan"></span>
            <span>专栏</span>
          </li>
          <li>
            <span class="iconfont icon-zhuanlan"></span>
            <span>专栏</span>
          </li>
          <li>
            <span class="iconfont icon-zhuanlan"></span>
            <span>专栏</span>
          </li>
          <li>
            <span class="iconfont icon-zhuanlan"></span>
            <span>专栏</span>
          </li>
          <li>
            <span class="iconfont icon-zhuanlan"></span>
            <span>专栏</span>
          </li>
        </ul>
      </div>
    </div>
    <div class="content">
      <div class="swiper">
        <el-carousel :interval="5000" arrow="always">
          <el-carousel-item v-for="item in 4" :key="item"> </el-carousel-item>
        </el-carousel>
      </div>
      <div class="contentmain">
        <ul>
          <li>
            <span>视频</span>
            <span>视频标题</span>
            <span>视频作者</span>
          </li>
          <li>
            <span>视频</span>
            <span>视频标题</span>
            <span>视频作者</span>
          </li>
          <li>
            <span>视频</span>
            <span>视频标题</span>
            <span>视频作者</span>
          </li>
          <li>
            <span>视频</span>
            <span>视频标题</span>
            <span>视频作者</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
let live = ref(false);
let game = ref(false);
let book = ref(false);
let download = ref(false);
let searchDialog = ref(false);
let userDialog = ref(false);

const searchFoucs = () => {
  let search = document.querySelector("input");
  let sear = document.querySelector(".search");
  search.style.backgroundColor = "rgb(227,229,231)";
  sear.style.borderBottomLeftRadius = "0px";
  sear.style.borderBottomRightRadius = "0px";
  searchDialog.value = true;
};
const searchBlur = () => {
  let search = document.querySelector("input");
  let sear = document.querySelector(".search");
  search.style.backgroundColor = "#f1f2f3";
  sear.style.borderBottomLeftRadius = "8px";
  sear.style.borderBottomRightRadius = "8px";
  searchDialog.value = false;
};
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 155px;
  background: url("../assets/img/header.png");
  background-position: center;
  background-size: cover;
  position: relative;
  .logo {
    width: 162px;
    height: 78px;
    background: url("../assets/img/logo.png");
    background-size: cover;
    position: absolute;
    bottom: 10px;
    left: 55px;
  }
  .header-nav {
    width: 100%;
    height: 64px;
    display: flex;
    align-items: center;
    margin: 0 2%;
    .menu {
      ul {
        display: flex;
        justify-content: center;
        align-items: center;
        li {
          color: #ffffff;
          font-size: 14px;
          margin-right: 10px;
          padding-bottom: 30px;
          padding-top: 30px;
          cursor: pointer;
        }
      }
    }
    .search {
      background: #f1f2f3;
      width: 385px;
      height: 40px;
      border-radius: 8px;
      margin-right: 5px;
      position: relative;
      span {
        position: absolute;
        bottom: 8px;
        right: 10px;
        color: #000;
        font-size: 20px;
      }
      input {
        width: 331px;
        height: 32px;
        margin: 4px 8px;
        background: #f1f2f3;
        border: 0;
        border-radius: 5px;
      }
      .shDialog {
        width: 385px;
        height: 600px;
        background: #f1f2f3;
        ul:first-child {
          display: flex;
          align-items: center;
          justify-content: space-between;
          margin: 0 15px;
          padding: 15px 0;
        }
        ul {
          display: flex;
          align-items: center;
          flex-wrap: wrap;
          li {
            text-align: center;
            line-height: 30px;
            height: 30px;
            background: #e3e5e5;
            border-radius: 5px;
            margin-left: 15px;
            margin-bottom: 10px;
            font-size: 12px;
          }
        }
        ol {
          list-style-type: decimal;
          list-style-position: inside;
          margin-left: 15px;
          h2 {
            font-size: 18px;
            margin: 15px 0;
          }
          li {
            margin-bottom: 20px;
          }
        }
      }
    }
    .user {
      ul {
        display: flex;
        justify-content: center;
        align-items: center;
        li {
          margin-left: 16px;
        }
        .user-img {
          position: relative;
          img {
            width: 40px;
            height: 40px;
            border: solid white 2px;
            border-radius: 50%;
            z-index: 999;
          }
          img:hover {
            animation: moveAndScale 0.8s ease-in-out forwards;
            position: relative;
          }
          .user-content {
            width: 300px;
            height: 450px;
            background: #ffffff;
            border-radius: 10px;
            position: absolute;
            left: -140px;
            top: 60px;
            text-align: center;
          }
        }
        @keyframes moveAndScale {
          0% {
            transform: translate(0, 0) scale(1);
          }
          50% {
            transform: translate(-10px, 25px) scale(1.6);
          }
          100% {
            transform: translate(-15px, 40px) scale(2.3);
          }
        }
        .user-upload {
          width: 34px;
          height: 34px;
          background: rgb(247, 120, 141);
          border-radius: 20%;
          text-align: center;
          line-height: 34px;
          margin-left: 25px;
        }
      }
    }
  }
  .live {
    width: 500px;
    height: 300px;
    background: #ffffff;
    border-radius: 10px;
    position: absolute;
    left: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    .live-left {
      flex: 6;
      img {
        width: 80px;
        height: 80px;
        border-radius: 50%;
        margin-right: 20px;
        margin-top: 20px;
      }
    }
    .live-right {
      flex: 4;
      img {
        width: 200px;
        height: 80px;
        border-radius: 5%;
        margin-top: 20px;
      }
    }
  }
  .game {
    width: 390px;
    height: 300px;
    background: #ffffff;
    border-radius: 10px;
    position: absolute;
    left: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    .game-left {
      flex: 7;
      img:first-child {
        width: 200px;
        height: 160px;
        margin-bottom: 20px;
      }
      img {
        width: 60px;
        height: 60px;
        margin-right: 10px;
      }
    }
    .game-right {
      flex: 3;
      text-align: center;
      h2 {
        font-size: 25px;
        margin-bottom: 30px;
      }
      ul {
        li {
          margin-bottom: 10px;
        }
      }
    }
  }
  .book {
    width: 450px;
    height: 280px;
    background: #ffffff;
    border-radius: 10px;
    position: absolute;
    left: 200px;
    display: flex;
    justify-content: center;
    align-items: center;
    .book-left {
      flex: 7;
      img {
        width: 140px;
        height: 100px;
        margin: 5px 5px;
      }
    }
    .book-right {
      text-align: left;
      flex: 3;
      h2 {
        font-size: 25px;
        margin-bottom: 30px;
      }
      ol {
        list-style-type: decimal;
        list-style-position: inside;
        li {
          margin-bottom: 15px;
        }
      }
    }
  }
  .download {
    width: 350px;
    height: 200px;
    background: #ffffff;
    border-radius: 10px;
    position: absolute;
    left: 350px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  .down-left {
    flex: 5;
    img {
      width: 100px;
      height: 100px;
      border: #61666d solid 1px;
      border-radius: 10px;
    }
    ul {
      li {
        margin-bottom: 10px;
      }
    }
  }
  .down-right {
    flex: 5;
    img {
      width: 60px;
      height: 60px;
    }
    ul {
      li {
        margin-bottom: 10px;
        button {
          background: rgb(11, 160, 224);
          border: 0;
          border-radius: 5px;
          height: 30px;
          width: 100px;
          color: #ffffff;
        }
      }
    }
  }
}
.icon1 {
  font-size: 24px;
  color: #ffffff;
}
.icon2 {
  font-size: 18px;
  color: #ffffff;
}
.icon3 {
  margin-right: 5px;
}
.category {
  width: 100%;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  .total {
    margin-left: 80px;
    display: flex;
    align-items: center;
    flex: 8;
    .left {
      margin-right: 15px;
      ul {
        display: flex;
        align-items: center;
        li {
          display: flex;
          flex-direction: column;
          font-size: 13px;
          margin-left: 15px;
          text-align: center;
          .icon {
            width: 35px;
            height: 35px;
          }
        }
      }
    }
    .center {
      ul {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        li {
          width: 67.22px;
          height: 28px;
          font-size: 13px;
          background: #f6f7f8;
          color: #61666d;
          border: solid rgb(205, 203, 203) 1px;
          border-radius: 5px;
          margin-right: 8px;
          margin-bottom: 8px;
          text-align: center;
          line-height: 28px;
        }
      }
    }
  }
  .right {
    flex: 2;
    margin-left: 10px;
    margin-right: 50px;
    ul {
      display: flex;
      flex-wrap: wrap;
      li {
        width: 60px;
        height: 28px;
        color: #61666d;
        font-size: 13px;
      }
    }
  }
}
.content {
  display: flex;
  justify-content: center;
  width: 100%;
  .swiper {
    margin-left: 100px;
    flex: 5;
    width: 585px;
    height: 382.69px;
    background: #61666d;
  }
  .contentmain {
    flex: 5;
    ul {
      display: flex;
      flex-wrap: wrap;
      li {
        width: 217.4px;
        height: 257.5px;
        display: flex;
        flex-direction: column;
        background: rgb(12, 192, 233);
        margin-left: 20px;
        margin-bottom: 10px;
      }
    }
  }
}
</style>