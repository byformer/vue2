<template>
  <div class="chat">
    <ul>
      <li class="active">
        <img src="../assets/pic1.svg" />
        <span>{{ all }}</span>
      </li>
      <li>
        <img src="../assets/pic2.svg" />
        <span>{{ vue }}</span>
      </li>

      <li>
        <img src="../assets/pic4.svg" />
        <span>{{ react }}</span>
      </li>
      <li>
        <img src="../assets/pic5.svg" />
        <span>{{ js }}</span>
      </li>
    </ul>
    <!-- 内容 -->
    <div class="content">
      <el-row type="flex" class="row-bg" justify="space-around">
        <el-col :span="7">
          <div class="grid-content bg-purple project">
            <span class="icon" style="background-color: rgb(69, 148, 8)"
              >V</span
            >
            <a href="javascript:;" target="_blanket">
              <strong>Vue-demo</strong>
              <p>
                这是一个Vue2.x的树组件。它允许你去拖拽任意节点，当然，“交换”会反映在data数据中。
              </p>
            </a>
          </div>
        </el-col>
        <el-col :span="7"
          ><div class="grid-content bg-purple-light project">
            <span class="icon" style="background-color: rgb(232, 239, 24)"
              >JS</span
            >
            <a href="javascript:;" target="_blanket">
              <strong>JS-demo</strong>
              <p>
                ----------------------------暂无内容----------------------------------
              </p>
            </a>
          </div>
        </el-col>
        <el-col :span="7"
          ><div class="grid-content bg-purple project">
            <span class="icon" style="background-color: rgb(20, 111, 246)"
              >R</span
            >
            <a href="javascript:;" target="_blanket">
              <strong>React-demo</strong>
              <p>
                ----------------------------暂无内容----------------------------------
              </p>
            </a>
          </div></el-col
        >
      </el-row>
    </div>
  </div>
</template>

<script>
export default {
  mounters: {},
  data() {
    return {
      all: "All Projects",
      vue: "Vue",
      js: "JavaScript",
      react: "React",
    };
  },
  mounted() {},
};
</script>

<style>
.chat {
  height: 500px;
  border-bottom: 1px solid #ccc;
}
.chat ul {
  display: flex;
  height: 50px;
  border-bottom: 1px solid rgb(231, 230, 230);
  margin-bottom: 50px;
  /* box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.1) */
  /* background-color: rgb(20, 111, 246) */
}
.chat ul li {
  margin: 0 15px;
  /* text-align: center; */
  display: flex;
  align-items: center;
  cursor: pointer;
}
.chat ul li img {
  width: 20px;
  height: 20px;
  vertical-align: middle;
}
.chat ul li span {
  text-align: center;
  padding-left: 10px;
}
/* 内容 */
.project {
  display: flex;
  align-items: center;
}
.project span {
  width: 80px;
  height: 40px;
  display: inline-block;
  margin-right: 10px;
  text-align: center;
  line-height: 40px;
  border-radius: 0.25rem;
  font-size: 1.25rem;
  color: #fff;
  font-weight: 700;
}
.project a strong {
  margin: 0 20px 0 10px;
}
.project a p {
  display: inline;
  font-weight: normal;
  width: 100px;
}
.active {
  border-bottom: 3px solid #e13f5e;
}
</style>