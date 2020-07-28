<template>
  <div id="app">
    <div>
      <img :src="item" v-for="(item, index) in arr" :key="index" style="width:50vw;"/>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      arr: [],
    };
  },
  created() {
    for (let index = 0; index < 513; index++) {
      this.arr.push(require(`../../images/100 (${index + 1}).gif`));
    }
  },
  mounted() {},
};
</script>

<style lang="less">
// less外部文件的使用
@import url("./assets/less/index");
</style>
