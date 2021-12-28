<template>
  <div class="home">

    <!-- 头部 -->
    <div class="head">
      <div class="headleft">
        <img class="icon" src="../assets/img/liebiao.png" alt="" />
        <span>大任务</span>
      </div>
      <div class="add">
        <img class="icon" src="../assets/img/add.png" alt="" />
      </div>
    </div>

    <!-- 计算参数和资料审查 -->
    <div class="container">
      <div class="left">
        <img class="icon" src="../assets/img/jisuan.png" alt="" />
        <span>计算参数</span>
      </div>
      <div class="left">
        <img class="icon" src="../assets/img/detail.png" alt="" />
        <span>资料审查</span>
      </div>

      <div class="right">
        <img class="icon" src="../assets/img/upload.png" alt="" />
      </div>
    </div>
    <!-- <LittleTask /> -->
  </div>
</template>

<script>
// import LittleTask from "../components/LittleTask.vue";
export default {
  //   components: { LittleTask },
};
</script>
<style scoped>
* {
  width: 750px;
  height: auto;
  font-size: 62.5%;
}
.home {
  width: 100%;
  margin: 0.5rem;
  color: #000;
  background-color: #fff;
}


.head {
    width: 100%;
  height: 8rem;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.head .icon {
  width: 3.5rem;
  height: 3.5rem;
}
.head span {
  font-size: 4rem;
  font-weight: bold;
}
.container {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  vertical-align: middle;
}
.container .left {
  height: 5rem;
  width: 30rem;
  font-size: 4rem;
  align-items: center;
  border: 1px solid #000;
}
.container .icon {
  width: 5rem;
  height: 5rem;
}
</style>