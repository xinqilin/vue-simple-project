<template>
  <div class="hello">
    <!-- 2. msg 雙向綁定到 template 的地方 -->
    <h1>{{ msg }}</h1>

    <!-- 4. 插入我們新增的數據看看，兩個 {{ }} 中可以綁定 data 任意值 -->
    <h2>{{ hello }}</h2>

    <!-- 5. 也可以撰寫一些 javascript code -->
    <h2>{{ hello +msg+ ' Bill practice 2020' }}</h2>

    <!-- 6. 加一個 input 來嘗試今天的任務，雙向綁定
    修改 input 裡面的值，綁定的地方也會馬上更新-->
    <input type="text" v-model="hello" />

    <!-- 8. 使用 checkbox 來完成雙向綁定 -->
    <input type="checkbox" v-model="toggle" />
    {{ toggle }}
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a href="https://vuejs.org" target="_blank">Core Docs</a>
      </li>
      <li>
        <a href="https://forum.vuejs.org" target="_blank">Forum</a>
      </li>
      <li>
        <a href="https://chat.vuejs.org" target="_blank">Community Chat</a>
      </li>
      <li>
        <a href="https://twitter.com/vuejs" target="_blank">Twitter</a>
      </li>
      <br />
      <li>
        <a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a>
      </li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li>
        <a href="http://router.vuejs.org/" target="_blank">vue-router</a>
      </li>
      <li>
        <a href="http://vuex.vuejs.org/" target="_blank">vuex</a>
      </li>
      <li>
        <a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a>
      </li>
      <li>
        <a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  // name: "hello",
  data() {
    return {
      // 1. data 這裡就是 model 存放一些資料
      // 這邊的資料與 tmplate 可以做雙向綁定
      msg: "Welcome to Your Vue.js App",
      // 3. 嘗試新增一個數據
      hello: "Hello Vue !",

      // 7. checkbox 預設是 false
      toggle: true
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
