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
    <div class="group" style="width: 100%">
      <sad-row >
        <sad-column span="8" >
          <div class="grid-content">8</div>
        </sad-column>
        <sad-column span="8">
          <div class="grid-content">8</div>
        </sad-column>
        <sad-column span="8">
          <div class="grid-content">8</div>
        </sad-column>
        <sad-column span="6" >
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="6">
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="6">
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="6">
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="4">
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4" >
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4">
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4">
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4">
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4" >
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
      </sad-row>
    </div>
    <div class="group" style="width: 100%">
      <sad-row gutter="10" >
        <sad-column span="8" >
          <div class="grid-content">8</div>
        </sad-column>
        <sad-column span="8">
          <div class="grid-content">8</div>
        </sad-column>
        <sad-column span="8">
          <div class="grid-content">8</div>
        </sad-column>
        <sad-column span="6" >
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="6">
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="6">
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="6">
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="4">
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4" >
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4">
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4">
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4">
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="4" >
          <div class="grid-content">4</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
        <sad-column span="2" >
          <div class="grid-content">2</div>
        </sad-column>
      </sad-row>
    </div>
    <div class="group" style="width: 100%">
      <sad-row>
        <sad-column span="8">
          <div class="grid-content">8</div>
        </sad-column>
        <sad-column span="8" offset="8">
          <div class="grid-content">8</div>
        </sad-column>
        <sad-column span="6" >
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="6" offset="6">
          <div class="grid-content">6</div>
        </sad-column>
        <sad-column span="6" >
          <div class="grid-content">6</div>
        </sad-column>
      </sad-row>
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
import sadColumn from './components/sad-column'
import sadRow from './components/sad-row'
 export default {
  name: 'app',
  components: {SadButton, SadInput, sadTabs, sadTabsBody, sadTabsHead, sadTabsPanel ,sadTabsItem, sadColumn, sadRow},
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
      padding: 20px;
      display: flex;
      flex-direction: row;
      > div {
        margin-right: 5px;
      }
      .grid-content{
        border: silver solid 1px;
        height: 40px;
        display: flex;
        align-items: center;
        justify-content: center;
      }
    }
  }
</style>
