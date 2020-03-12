<template>
  <div id="app">
    <div class="group">
      <div>
        <sad-button >默认按钮</sad-button>
      </div>
      <div>
        <sad-button icon="settings">icon按钮</sad-button>
      </div>
      <div>
        <sad-button icon="left">icon按钮</sad-button>
      </div>
      <div>
        <sad-button icon="settings" icon-position="right" @click="click('Button | icon = setting | icon-position = right')">icon居右按钮</sad-button>
      </div>
    </div>
    <div class="group">
      <div>
        <sad-input value='禁用' disabled/>
      </div>
      <div>
        <sad-input value='只读' readonly/>
      </div>
      <div>
        <sad-input error='出错了'/>
      </div>
      <div>
        <sad-input  v-model="value" :value="value"/> value: {{value}}
      </div>
    </div>
  </div>
</template>

<script>
import SadButton from './components/sad-button'
import SadInput from './components/sad-input'
export default {
  name: 'app',
  components: {SadButton, SadInput},
  data:()=>{
    return{
      value: '支持双向绑定'
    }
  },
  methods: {
    click(x){
      console.log(x)
    }
  }
}
</script>

<style lang="scss">
  #app {
    .group{
      margin: 20px;
      display: flex;
      flex-direction: row;
      div {
        margin-right: 5px;
      }
    }
  }
</style>
