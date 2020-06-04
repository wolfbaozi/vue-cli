<template>
  <button @click="fatherclick">你爹让你点了？</button>
</template>

<script>
export default {
  name: "children",
  methods: {
    fatherclick: function() {
      this.$parent.fatherclick();
      console.log("1");
    }
  }
};
</script>

<style>
</style>