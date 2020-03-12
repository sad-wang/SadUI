<template>
  <div id="app">
    <sad-button >默认按钮</sad-button>
    <sad-button icon="settings">icon按钮</sad-button>
    <sad-button icon="left">icon按钮</sad-button>
    <sad-button icon="settings" icon-position="right">icon居右按钮</sad-button>
  </div>
</template>

<script>
import SadButton from "./components/sad-button";
export default {
  name: "app",
  components: {SadButton}
}
</script>

<style lang="scss">
  * {margin: 0; padding: 0; box-sizing: border-box;}
  html {
    --button-height: 32px;
    --font-size: 14px;
    --button-bg: white;
    --button-active-bg: #eee;
    --border-radius: 4px;
    --color: #333;
    --border-color: #999;
    --border-color-hover: #666;
  }
  #app {
    margin: 20px;
  }
  body {
    font-size: var(--font-size);
  }
</style>
