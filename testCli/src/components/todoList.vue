<template>
  <div class="app">
    <child></child>
    <div>
      <input v-model="value" />
      <button @click="submit(value)">提交</button>
    </div>
    <todoItem :list="list" @delect="listdelect"></todoItem>
  </div>
</template>
<script>
import todoItem from "./todoItem";
import child from "./children";
export default {
  components: {
    todoItem,
    child
  },
  data: function() {
    return {
      msg: "hello",
      value: "",
      list: []
    };
  },
  methods: {
    submit: function(value) {
      if (!value.length) {
        alert("啥都不填，你提交你妈呢,刘国辉");
        return;
      }
      this.list.push(value);
      this.value = "";
    },
    listdelect: function(index) {
      this.list.splice(index, 1);
    },
    fatherclick: function() {
      alert("我是你爸爸");
    }
  }
};
</script>