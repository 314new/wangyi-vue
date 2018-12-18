<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
  export default {
    name: 'wangyi'
  }
</script>

<style>
  /* CSS */
  * {
    padding: 0;
    margin: 0;
  }
  html {
    width: 100vw;
    height: 100vh;
    padding: 5px;
    box-sizing: border-box;
    background: transparent;
  }
  body {
    height: 100%;
    height: 100%;
    border-radius: 5px;
    box-shadow: 0 0 2px 1px rgba(0, 0, 0, 0.2), 0 0 5px 2px rgba(0, 0, 0, 0.1);
  }
  #app {
    display: flex;
    height: 100%;
    width: 100%;
  }
  /* 修改原有的样式 */
  .coustom-scroll-bar::-webkit-scrollbar {
    width: 4px;
  }
  .coustom-scroll-bar::-webkit-scrollbar-thumb {
    background: rgba(0,0,0,0.3);
    border-radius: 4px;
  }
  .coustom-scroll-bar::-webkit-scrollbar-thumb:hover {
    background: rgba(0,0,0,0.8);
    transition: 1s all;
  } 
  a {
    outline: none;
    text-decoration: none;
    color: #000;
  }
</style>
