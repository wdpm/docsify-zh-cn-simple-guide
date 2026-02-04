# 兼容 Vue

可以直接在 Markdown 文件里写 Vue 代码，它将被执行。


## 美化版本

<div id="styled-demo"></div>

<script>
Vue.createApp({
  data() {
    return {
      message: 'Hello Vue 3 in Docsify! 🎉',
      count: 0
    };
  },
  template: `
    <div style="
      padding: 20px;
      margin: 20px 0;
      border: 2px solid #42b983;
      border-radius: 10px;
      background: #f8fff8;
    ">
      <h3 style="color: #2c3e50; margin-top: 0;">Vue 3 Component</h3>
      <p style="font-size: 18px; color: #42b983;">{{ message }}</p>
      <p>Count: <strong>{{ count }}</strong></p>
      <div style="margin-top: 15px;">
        <button @click="count++"
          style="
            padding: 8px 16px;
            margin-right: 10px;
            background: #42b983;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
          "
        >
          Increment
        </button>
        <button @click="count = 0"
          style="
            padding: 8px 16px;
            background: #f56c6c;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
          "
        >
          Reset
        </button>
      </div>
    </div>
  `
}).mount('#styled-demo');
</script>