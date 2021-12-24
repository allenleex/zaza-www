<template>
  <div id="app">
    <nav>
      <ul>
        <li><a href="#first">首页</a></li>
        <li><a href="#second">产品下载</a></li>
        <li><a href="#third">虚拟偶像</a></li>
        <li><a href="#fourth">关于我们</a></li>
      </ul>
    </nav>

    <video-player
      id="first"
      class="video-player-box"
      ref="videoPlayer"
      :options="playerOptions"
      :playsinline="true"
    >
    </video-player>

    <section id="second">
      <h1>产品下载</h1>
      <div class="container">
        <div class="row">
          <div class="col-sm-6 col-md-4">
            <div class="thumbnail">
              <img
                data-src="holder.js/100%x200"
                alt="100%x200"
                src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9InllcyI/PjxzdmcgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB3aWR0aD0iMjQyIiBoZWlnaHQ9IjIwMCIgdmlld0JveD0iMCAwIDI0MiAyMDAiIHByZXNlcnZlQXNwZWN0UmF0aW89Im5vbmUiPjwhLS0KU291cmNlIFVSTDogaG9sZGVyLmpzLzEwMCV4MjAwCkNyZWF0ZWQgd2l0aCBIb2xkZXIuanMgMi42LjAuCkxlYXJuIG1vcmUgYXQgaHR0cDovL2hvbGRlcmpzLmNvbQooYykgMjAxMi0yMDE1IEl2YW4gTWFsb3BpbnNreSAtIGh0dHA6Ly9pbXNreS5jbwotLT48ZGVmcz48c3R5bGUgdHlwZT0idGV4dC9jc3MiPjwhW0NEQVRBWyNob2xkZXJfMTdkZWI1NWFiYzkgdGV4dCB7IGZpbGw6I0FBQUFBQTtmb250LXdlaWdodDpib2xkO2ZvbnQtZmFtaWx5OkFyaWFsLCBIZWx2ZXRpY2EsIE9wZW4gU2Fucywgc2Fucy1zZXJpZiwgbW9ub3NwYWNlO2ZvbnQtc2l6ZToxMnB0IH0gXV0+PC9zdHlsZT48L2RlZnM+PGcgaWQ9ImhvbGRlcl8xN2RlYjU1YWJjOSI+PHJlY3Qgd2lkdGg9IjI0MiIgaGVpZ2h0PSIyMDAiIGZpbGw9IiNFRUVFRUUiLz48Zz48dGV4dCB4PSI4OS44NTE1NjI1IiB5PSIxMDUuMzYyNSI+MjQyeDIwMDwvdGV4dD48L2c+PC9nPjwvc3ZnPg=="
                data-holder-rendered="true"
                style="height: 200px; width: 100%; display: block"
              />
              <div class="caption">
                <h3>基础版</h3>
                <p>
                  在这里放置一段产品说明文字<br />在这里放置一段产品说明文字<br />在这里放置一段产品说明文字
                </p>
                <p>
                  <button type="button" class="btn btn-warning btn-lg">
                    立即下载 (Windows10版本)
                  </button>
                </p>
              </div>
            </div>
          </div>
          <div class="col-sm-6 col-md-4">
            <div class="thumbnail">
              <img
                data-src="holder.js/100%x200"
                alt="100%x200"
                src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9InllcyI/PjxzdmcgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB3aWR0aD0iMjQyIiBoZWlnaHQ9IjIwMCIgdmlld0JveD0iMCAwIDI0MiAyMDAiIHByZXNlcnZlQXNwZWN0UmF0aW89Im5vbmUiPjwhLS0KU291cmNlIFVSTDogaG9sZGVyLmpzLzEwMCV4MjAwCkNyZWF0ZWQgd2l0aCBIb2xkZXIuanMgMi42LjAuCkxlYXJuIG1vcmUgYXQgaHR0cDovL2hvbGRlcmpzLmNvbQooYykgMjAxMi0yMDE1IEl2YW4gTWFsb3BpbnNreSAtIGh0dHA6Ly9pbXNreS5jbwotLT48ZGVmcz48c3R5bGUgdHlwZT0idGV4dC9jc3MiPjwhW0NEQVRBWyNob2xkZXJfMTdkZWI1NjBlZWYgdGV4dCB7IGZpbGw6I0FBQUFBQTtmb250LXdlaWdodDpib2xkO2ZvbnQtZmFtaWx5OkFyaWFsLCBIZWx2ZXRpY2EsIE9wZW4gU2Fucywgc2Fucy1zZXJpZiwgbW9ub3NwYWNlO2ZvbnQtc2l6ZToxMnB0IH0gXV0+PC9zdHlsZT48L2RlZnM+PGcgaWQ9ImhvbGRlcl8xN2RlYjU2MGVlZiI+PHJlY3Qgd2lkdGg9IjI0MiIgaGVpZ2h0PSIyMDAiIGZpbGw9IiNFRUVFRUUiLz48Zz48dGV4dCB4PSI4OS44NTE1NjI1IiB5PSIxMDUuMzYyNSI+MjQyeDIwMDwvdGV4dD48L2c+PC9nPjwvc3ZnPg=="
                data-holder-rendered="true"
                style="height: 200px; width: 100%; display: block"
              />
              <div class="caption">
                <h3>专业版</h3>
                <p>
                  在这里放置一段产品说明文字<br />在这里放置一段产品说明文字<br />在这里放置一段产品说明文字
                </p>
                <h2>敬请期待</h2>
              </div>
            </div>
          </div>
          <div class="col-sm-6 col-md-4">
            <div class="thumbnail">
              <img
                data-src="holder.js/100%x200"
                alt="100%x200"
                src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9InllcyI/PjxzdmcgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB3aWR0aD0iMjQyIiBoZWlnaHQ9IjIwMCIgdmlld0JveD0iMCAwIDI0MiAyMDAiIHByZXNlcnZlQXNwZWN0UmF0aW89Im5vbmUiPjwhLS0KU291cmNlIFVSTDogaG9sZGVyLmpzLzEwMCV4MjAwCkNyZWF0ZWQgd2l0aCBIb2xkZXIuanMgMi42LjAuCkxlYXJuIG1vcmUgYXQgaHR0cDovL2hvbGRlcmpzLmNvbQooYykgMjAxMi0yMDE1IEl2YW4gTWFsb3BpbnNreSAtIGh0dHA6Ly9pbXNreS5jbwotLT48ZGVmcz48c3R5bGUgdHlwZT0idGV4dC9jc3MiPjwhW0NEQVRBWyNob2xkZXJfMTdkZWI1NWM3M2QgdGV4dCB7IGZpbGw6I0FBQUFBQTtmb250LXdlaWdodDpib2xkO2ZvbnQtZmFtaWx5OkFyaWFsLCBIZWx2ZXRpY2EsIE9wZW4gU2Fucywgc2Fucy1zZXJpZiwgbW9ub3NwYWNlO2ZvbnQtc2l6ZToxMnB0IH0gXV0+PC9zdHlsZT48L2RlZnM+PGcgaWQ9ImhvbGRlcl8xN2RlYjU1YzczZCI+PHJlY3Qgd2lkdGg9IjI0MiIgaGVpZ2h0PSIyMDAiIGZpbGw9IiNFRUVFRUUiLz48Zz48dGV4dCB4PSI4OS44NTE1NjI1IiB5PSIxMDUuMzYyNSI+MjQyeDIwMDwvdGV4dD48L2c+PC9nPjwvc3ZnPg=="
                data-holder-rendered="true"
                style="height: 200px; width: 100%; display: block"
              />
              <div class="caption">
                <h3>旗舰版</h3>
                <p>
                  在这里放置一段产品说明文字<br />在这里放置一段产品说明文字<br />在这里放置一段产品说明文字
                </p>
                <h2>敬请期待</h2>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="third">
      <h1>虚拟偶像</h1>
      <div class="container">
        <div class="row">
          <div class="col-sm-2 col-md-2">
            <div class="thumbnail">
              <img
                data-src="holder.js/200%x200"
                alt="100%x200"
                src="https://images-common.oss-cn-guangzhou.aliyuncs.com/video/78FFDEE8-CA0D-4AD1-AAB3-BA7936168E3E.png"
                data-holder-rendered="true"
                style="width: 100%; display: block"
              />
              <div class="caption">
                <h4>偶像名称</h4>
              </div>
            </div>
          </div>
          <div class="col-sm-2 col-md-2">
            <div class="thumbnail">
              <img
                data-src="holder.js/200%x200"
                alt="100%x200"
                src="https://images-common.oss-cn-guangzhou.aliyuncs.com/video/78FFDEE8-CA0D-4AD1-AAB3-BA7936168E3E.png"
                data-holder-rendered="true"
                style="width: 100%; display: block"
              />
              <div class="caption">
                <h4>偶像名称</h4>
              </div>
            </div>
          </div>
          <div class="col-sm-2 col-md-2">
            <div class="thumbnail">
              <img
                data-src="holder.js/200%x200"
                alt="100%x200"
                src="https://images-common.oss-cn-guangzhou.aliyuncs.com/video/78FFDEE8-CA0D-4AD1-AAB3-BA7936168E3E.png"
                data-holder-rendered="true"
                style="width: 100%; display: block"
              />
              <div class="caption">
                <h4>偶像名称</h4>
              </div>
            </div>
          </div>
          <div class="col-sm-2 col-md-2">
            <div class="thumbnail">
              <img
                data-src="holder.js/200%x200"
                alt="100%x200"
                src="https://images-common.oss-cn-guangzhou.aliyuncs.com/video/78FFDEE8-CA0D-4AD1-AAB3-BA7936168E3E.png"
                data-holder-rendered="true"
                style="width: 100%; display: block"
              />
              <div class="caption">
                <h4>偶像名称</h4>
              </div>
            </div>
          </div>
          <div class="col-sm-2 col-md-2">
            <div class="thumbnail">
              <img
                data-src="holder.js/200%x200"
                alt="100%x200"
                src="https://images-common.oss-cn-guangzhou.aliyuncs.com/video/78FFDEE8-CA0D-4AD1-AAB3-BA7936168E3E.png"
                data-holder-rendered="true"
                style="width: 100%; display: block"
              />
              <div class="caption">
                <h4>偶像名称</h4>
              </div>
            </div>
          </div>
          <div class="col-sm-2 col-md-2">
            <div class="thumbnail">
              <img
                data-src="holder.js/200%x200"
                alt="100%x200"
                src="https://images-common.oss-cn-guangzhou.aliyuncs.com/video/78FFDEE8-CA0D-4AD1-AAB3-BA7936168E3E.png"
                data-holder-rendered="true"
                style="width: 100%; display: block"
              />
              <div class="caption">
                <h4>偶像名称</h4>
              </div>
            </div>
          </div>
          <div class="col-sm-2 col-md-2">
            <div class="thumbnail">
              <img
                data-src="holder.js/200%x200"
                alt="100%x200"
                src="https://images-common.oss-cn-guangzhou.aliyuncs.com/video/78FFDEE8-CA0D-4AD1-AAB3-BA7936168E3E.png"
                data-holder-rendered="true"
                style="width: 100%; display: block"
              />
              <div class="caption">
                <h4>偶像名称</h4>
              </div>
            </div>
          </div>
          <div class="col-sm-2 col-md-2">
            <div class="thumbnail">
              <img
                data-src="holder.js/200%x200"
                alt="100%x200"
                src="https://images-common.oss-cn-guangzhou.aliyuncs.com/video/78FFDEE8-CA0D-4AD1-AAB3-BA7936168E3E.png"
                data-holder-rendered="true"
                style="width: 100%; display: block"
              />
              <div class="caption">
                <h4>偶像名称</h4>
              </div>
            </div>
          </div>
          <div class="col-sm-2 col-md-2">
            <div class="thumbnail">
              <img
                data-src="holder.js/200%x200"
                alt="100%x200"
                src="https://images-common.oss-cn-guangzhou.aliyuncs.com/video/78FFDEE8-CA0D-4AD1-AAB3-BA7936168E3E.png"
                data-holder-rendered="true"
                style="width: 100%; display: block"
              />
              <div class="caption">
                <h4>偶像名称</h4>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="fourth" class="container">
      <h1>关于我们</h1>
      <div id="fourth" class="jumbotron">
        <h1>Hello, world!</h1>
        <p>...</p>
        <p>
          <a class="btn btn-primary btn-lg" href="#" role="button"
            >Learn more</a
          >
        </p>
      </div>
    </section>

    <footer class="bs-docs-footer">
      <div class="container">
        <div class="row">
          <div class="col-md-6 text-left">
            <ul class="bs-docs-footer-links">
              <li><a href="#first">首页</a></li>
              <li><a href="#second">产品下载</a></li>
              <li><a href="#third">虚拟偶像</a></li>
              <li><a href="#fourth">关于我们</a></li>
            </ul>
          </div>
          <div class="col-md-6 text-right">
            <p>
              &copy; 2021-2025 
              广州喳喳科技有限公司, 版权所有.
              <a href="http://beian.miit.gov.cn/" target="_blank"
                >粤ICP备2021170452号-1</a
              >
            </p>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      playerOptions: {
        // videojs options
        controls: false,
        autoplay: true,
        muted: true,
        loop: true,
        preload: "auto",
        language: "zh-CN",
        aspectRatio: "16:9",
        fluid: true,
        playbackRates: [0.7, 1.0, 1.5, 2.0],
        sources: [
          {
            type: "video/mp4",
            src: "https://images-common.oss-cn-guangzhou.aliyuncs.com/video/bg1.mp4",
          },
        ],
        notSupportedMessage: "此视频暂无法播放，请稍后再试",
      },
    };
  },
  mounted() {
    console.log("this is current player instance object", this.player);
  },
  methods: {},
};
</script>

<style>
html {
  margin: 0;
  padding: 0;
  scroll-behavior: smooth;
}
body {
  background-color: black;
  margin: 0 0;
  padding: 0 0;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0 0;
  padding: 0 0;
}
.video-player-box {
  max-width: 100%;
}
.hidden {
  display: none;
}
nav {
  position: fixed;
  top: 0;
  width: 100vw;
  z-index: 9999;
  background-color: rgba(0, 0, 0, 0.75);
}
nav ul {
  width: 100%;
  display: flex;
  justify-content: center;
  box-sizing: border-box;
  padding: 10px 20px;
}
nav ul li {
  list-style: none;
  font-size: 16px;
  font-weight: bold;
}
nav ul li a {
  text-decoration: none;
  color: #808080;
  padding: 0 30px;
}
nav ul li a:hover {
  text-decoration: none;
  color: #f0f0f0;
}
section {
  /* height: 100vh; */
  display: grid;
  place-items: center;
  font-size: 20px;
  font-weight: bold;
  padding: 30px 0;
}
h1 {
  color: #808080;
  font-size: 24px;
  font-weight: 600;
  padding: 20px 0;
}
.caption {
  padding: 10px 0;
}
.caption p {
  margin: 20px 0;
  font-size: 16px;
}
.jumbotron {
  width: 100%;
}
.thumbnail {
  background-color: rgba(0, 0, 0, 0.75);
  border: none;
}
.thumbnail .caption {
  color: #808080;
}
.thumbnail .caption:hover {
  color: #f0f0f0;
}
.panel-body {
  font-size: 14px;
  text-align: left;
}
.text-left {
  text-align: left;
}
.text-center {
  text-align: center;
}
.text-right {
  text-align: right;
}
</style>
