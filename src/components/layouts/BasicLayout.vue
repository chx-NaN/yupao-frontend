<template>
  <van-nav-bar
  title="标题"

  left-arrow
  @click-left="onClickLeft"
  @click-right="onClickRight"
>
  <template #right>
    <van-icon name="search" size="18" />
  </template>
</van-nav-bar>
<van-tabbar v-model="active" @change="onChange">
  <van-tabbar-item icon="home-o" name="index">主页</van-tabbar-item>
  <van-tabbar-item icon="search" name="team">队伍</van-tabbar-item>
  <van-tabbar-item icon="friends-o" name="user">个人</van-tabbar-item>

</van-tabbar>
</template>

<script setup>
import { Toast } from 'vant';
import { ref } from 'vue';
const onClickLeft = () => alert("左");
const onClickRight = () => alert("右");
const active = ref(0);
const onChange = (index) => Toast(`标签 ${index}`);
// export default {
  
// };
</script>

<style>

</style>