<template>
  <div>
    <ul>
      <li v-for="(item,index) in list" :key="index">
        {{item}}
        <span @click="delect(index)">删除</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "todoItem",
  props: ["list"],
  data() {
    return {
      root: "awsl"
    };
  },
  methods: {
    delect: function(index) {
      this.$emit("delect", index);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
