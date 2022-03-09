<template>
  <div>
    <div><p v-if="seen">你能看到我</p></div>
    <div>
      <ol>
        <li v-for="(todo,index) in todos" :key="index">
          {{todo.text}}
        </li>
      </ol>
    </div>
<div>
  <p>{{message}}</p>
  <button v-on:click="reverseMessage()">反转消息</button>
</div>
<div>
  <p>{{messages}}</p>
  <input type="text" v-model="messages">
</div>
<div>
  <button @click="ceshi()">测试</button>
</div>
<div>
  <span v-once>这个将不会改变{{msg}}</span>
</div>

<div>
  <p>Using mustaches:{{rawHtml}}</p>
  <p>Using V-html directive: <span v-html="rawHtml"></span></p>
  <p></p>
</div>
  </div>

</template>

<script>
export default {
  name:'Test2',

  data() {
    return{
      seen:true,
      todos:[
        {text:"学习javascript"},
        {text:"学习java"},
        {text:"学习css"}
      ],
      message:"这是一句话",
      messages:"你好，vue",
      msg:"会不会",
      rawHtml:"This should be red",
    }

  },
  methods:{
    reverseMessage(){
      this.message=this.message.split('').reverse().join('')

    },
    ceshi(){
      var str =new Array("高山","流水","大珠小珠落玉盘","犹抱琵琶半遮面");
      console.log(str);

      var object = {网址:"www.baidu.com",负责人:"王大锤"};
      console.log(object);
    }

  }



}

</script>

<style scoped>

</style>
