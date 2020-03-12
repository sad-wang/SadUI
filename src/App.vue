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
    <div>
      <sad-tabs selected="finance" >
        <sad-tabs-head >
          <sad-tabs-item name="disabled" disabled >
            不可用
          </sad-tabs-item>
          <sad-tabs-item name="finance">
            财经
          </sad-tabs-item>
          <sad-tabs-item name="sports">
            体育
          </sad-tabs-item>
        </sad-tabs-head>
        <sad-tabs-body>
          <sad-tabs-panel name="disabled">
            相关资讯
          </sad-tabs-panel>
          <sad-tabs-panel name="finance">
            财经相关资讯
          </sad-tabs-panel>
          <sad-tabs-panel name="sports">
            体育相关资讯
          </sad-tabs-panel>
        </sad-tabs-body>
      </sad-tabs>
    </div>
  </div>
</template>

<script>
import SadButton from './components/sad-button'
import SadInput from './components/sad-input'
import sadTabs from './components/sad-tabs'
import sadTabsBody from './components/sad-tabs-body'
import sadTabsHead from './components/sad-tabs-head'
import sadTabsItem from './components/sad-tabs-item'
import sadTabsPanel from './components/sad-tabs-panel'
export default {
  name: 'app',
  components: {SadButton, SadInput, sadTabs, sadTabsBody, sadTabsHead, sadTabsPanel ,sadTabsItem},
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
