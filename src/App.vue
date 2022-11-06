<template>
  <div class="continuer">
    <!-- 头部 -->
    <header>
      <div class="header">
        <el-row type="flex" class="row-bg" justify="space-between">
          <el-col :span="6"
            ><div class="grid-content bg-purple bg-left bg-header">
              <h1 class="h1">Hello,World!</h1>
            </div></el-col
          >

          <el-col :span="12"
            ><div class="grid-content bg-purple bg-right bg-header">
              <li>
                <a href="javascript:;">{{ home }}</a>
              </li>
              <li>
                <a href="javascript:;">{{ blog }}</a>
              </li>
              <li>
                <a href="javascript:;">{{ github }}</a>
              </li>
              <li>
                <a href="javascript:;">{{ about }}</a>
              </li>
              <li>
                <a href="javascript:;">{{ resume }}</a>
              </li>
            </div></el-col
          >
        </el-row>
      </div>
    </header>
    <!-- 内容 -->
    <section>
      <el-row type="flex" class="row-bg bg-set" justify="space-around">
        <el-col :span="7" class="set"
          ><div class="grid-content bg-purple set-left">
            <p>
              {{ h1 }}
              <br />
              {{ h2 }}
              <br />
              {{ h3 }}
              <br />
              {{ h4 }}
              <br />
              <br />
              {{ h5 }}
              <br />
              {{ h6 }}
              <br />
              {{ h7 }}
              <br />
            </p></div
        ></el-col>

        <el-col :span="13"
          ><div class="grid-content bg-purple set-right">
            <page></page></div
        ></el-col>
      </el-row>
    </section>
    <!-- 底部 -->

    <buyCat></buyCat>

    <footer>
      <p> {{by}}</p>
     <a href="mailto:1633852615@qq.com" target="_blanket">
      <img src="./assets/pic6.svg" alt="">
      <span>{{email}}</span>
     </a>
    </footer>
  </div>
</template>

<script>
import page from "./components/page.vue";
import buyCat from "./components/buyCat.vue";

// import typing from './components/typing.vue';
export default {
  components: {
    page,
    buyCat,
  },
  data() {
    return {
      h1: "谎言的代价是什么？",
      h2: "并非是我们会把谎言误认为真相。",
      h3: "真正危险的是，",
      h4: "我们听多了谎言，便不再能分辨出真相。",
      h5: "那时我们能做什么？",
      h6: "除了放弃对真理的信仰，满足于谎言堆砌的故事。",
      h7: "我们还剩下什么？",
      home: "Home",
      blog: "Blog",
      github: "GitHub",
      about: "About",
      resume: "Resume",
      by:'Powered by PProfile',
      email:'1633852615@qq.com'
    };
  },
  modules: {},
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
li {
  list-style: none;
}
a {
  text-decoration: none;
  color: #000;
}
header {
  position: relative;
  height: 80px;
  background-color: #fff;
  z-index: 20;
}
.header {
  position: fixed;
  background-color: #fff;
  width: 100vw;
  height: 80px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
}
.bg-header {
  height: 80px;
}
.bg-left {
  display: flex;
  justify-content: center;
  align-items: center;
}
.bg-purple .h1 {
  color: #161b3d;
  font-size: 35px;
}
.bg-right {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
/* section */
section {
  height: 523px;
  background-color: #f8f8f8;
}
.bg-set {
  height: 500px;
  padding-top: 50px;
}

.set-left {
  position: relative;
}
.set-left p {
  position: absolute;
  top: 25px;
  left: 25px;
  font-size: 20px;
  line-height: 35px;
}
/* footer */

footer {
  height: 50px;
  padding: 1rem 2rem;
  display:flex;
  justify-content:space-between;
}
footer p{
  color:#919296;
}
footer a{
  display: flex;
}
footer a img{
  width: 20px;height:20px;
  vertical-align: middle;
}
footer a span{
  color:#919296;
  margin-left:10px;
}
</style>