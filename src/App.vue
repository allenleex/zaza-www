<template>
  <div id="app">
    <!-- <div class="container-fluid header">
      <div class="navbar-header">
        <button
          type="button"
          class="navbar-toggle collapsed"
          data-toggle="collapse"
          data-target="#bs-example-navbar-collapse-6"
          aria-expanded="false"
        >
          <span class="sr-only">切换</span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
        <a class="navbar-brand" href="#">动捕精灵</a>
      </div>

      <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-6">
        <ul class="nav navbar-nav">
          <li class="active"><a href="#">概况</a></li>
          <li><a href="#">下载</a></li>
          <li><a href="#">支持</a></li>
          <li><a href="#">关于</a></li>
        </ul>
      </div>
    </div> -->

    <nav>
      <ul>
        <li><a href="#first">首页</a></li>
        <li><a href="#second">下载</a></li>
        <li><a href="#third">支持</a></li>
        <li><a href="#fourth">关于</a></li>
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
      <div class="container gallery">
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
                <h3>Thumbnail label</h3>
                <p>
                  Cras justo odio, dapibus ac facilisis in, egestas eget quam.
                  Donec id elit non mi porta gravida at eget metus. Nullam id
                  dolor id nibh ultricies vehicula ut id elit.
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
                <h3>Thumbnail label</h3>
                <p>
                  Cras justo odio, dapibus ac facilisis in, egestas eget quam.
                  Donec id elit non mi porta gravida at eget metus. Nullam id
                  dolor id nibh ultricies vehicula ut id elit.
                </p>
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
                <h3>Thumbnail label</h3>
                <p>
                  Cras justo odio, dapibus ac facilisis in, egestas eget quam.
                  Donec id elit non mi porta gravida at eget metus. Nullam id
                  dolor id nibh ultricies vehicula ut id elit.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="third">Third Section</section>

    <section id="fourth">Fourth Section</section>

    <footer class="bs-docs-footer">
      <div class="container">
        <ul class="bs-docs-footer-links">
          <li><a href="https://github.com/twbs/bootstrap">GitHub</a></li>
          <li><a href="https://twitter.com/getbootstrap">Twitter</a></li>
          <li><a href="/getting-started/#examples">实例</a></li>
          <li><a href="/about/">关于</a></li>
        </ul>
        <p>Designed and built with all the love in the world by <a href="https://twitter.com/mdo" rel="noopener" target="_blank">@mdo</a> and <a href="https://twitter.com/fat" rel="noopener" target="_blank">@fat</a>. Maintained by the <a href="https://github.com/orgs/twbs/people">core team</a> with the help of <a href="https://github.com/twbs/bootstrap/graphs/contributors">our contributors</a>.</p>
        <p>Code licensed <a href="https://github.com/twbs/bootstrap/blob/v3-dev/LICENSE" rel="license noopener" target="_blank">MIT</a>, docs <a href="https://creativecommons.org/licenses/by/3.0/" rel="license noopener" target="_blank">CC BY 3.0</a>.</p>
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
  background-color: rgba(0,0,0,0.75);
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
.gallery {
  margin-top: 30px;
}
</style>
