<!--
 * @Author: xiaoxinYy 3037686283@qq.com
 * @Date: 2023-02-14 14:07:02
 * @LastEditors: Crayon 3037686283@qq.com
 * @LastEditTime: 2023-03-01 22:45:26
 * @FilePath: \SSR\01_node-server\src\App.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
  <div class="app" style="border: 1px solid pink">
    <h2>Vue3 App</h2>
    <div>{{ counter }}</div>
    <button @click="addCounter">+1</button>

    <div>
      <router-link to='/'>
        <button>首页</button>
      </router-link>
      <router-link to='/about'>
        <button>About</button>
      </router-link>
      <router-view></router-view>
    </div>
  </div>
</template>

<script setup>
  import { ref } from 'vue'
  const counter = ref(100)
  function addCounter () {
    counter.value ++
  }
</script>