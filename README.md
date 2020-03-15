# sadui
SadUI 是王 sad 为巩固 Vue 知识的使用而做的一个 UI 框架，希望对你有用。
最初版本 v0.1.0 已经发布到 npm。

## 技术栈
Vue CLI + Scss

## 安装
```npm
npm install sadui
```

## 使用
注意：
* 本 UI 库为 Vue UI 库。
* 由于本 UI 库开发未完成，使用时需要自行 Babel 转义 并安装 Scss* 由于本 UI 库开发未完成，使用时需要自行 Babel 转义 并安装 Scss。
### 克隆仓库预览
可在 `/src/App.vue` 中查看如何使用 UI 组件
```npm
git clone https://github.com/sad-wang/SadUI.git
npm install
npm run serve
```
### 安装UI库
```
npm install sadui
```
## 按钮 button
![sadButton](https://user-gold-cdn.xitu.io/2020/3/15/170db77b845f2064?w=476&h=59&f=png&s=4631)
```javascript
import { sadButton } from 'sadui'

<sad-button >默认按钮</sad-button>
<sad-button icon="settings">icon按钮</sad-button>
<sad-button icon="left">icon按钮</sad-button>
<sad-button icon="settings" icon-position="right" @click="bindfunction(x)">icon居右按钮</sad-button>
```
实现了一个 button 组件，可以根据 icon 属性来设置 icon，根据 icon-position 属性设置 icon 位置，可以绑定事件。

## 双向绑定输入框 input
![sadInput](https://user-gold-cdn.xitu.io/2020/3/15/170db79edef830e7?w=876&h=60&f=png&s=4835)
```javascript
import { sadInput } from 'sadui'

<sad-input value='禁用' disabled/>
<sad-input value='只读' readonly/>
<sad-input error='出错了'/>
<sad-input  v-model="value" :value="value"/> value: {{value}}

data:()=>{
  return{
    value: '支持双向绑定'
  }
},
```
实现了一个 input 组件，可以根据 disabled、readonly、error 属性实现不同 inpput 状态样式，实现了组件的双向绑定。

## 导航 tab
![sadTabs](https://user-gold-cdn.xitu.io/2020/3/15/170db7d0f769712f?w=356&h=51&f=png&s=1666)
```javascript
import {  sadTabs,sadTabsBody,sadTabsHead,sadTabsPanel,sadTabsItem, } from 'sadui'

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
```
通过利用 vue 实例当作 eventHub 实现组件事件的监听和触发，实现简单的 tabs 组件。
设置 name 属性一一对应 tab-item  和 tab-panel
## Grid 布局
![sadGrid](https://user-gold-cdn.xitu.io/2020/3/15/170db82b1a042e44?w=1023&h=185&f=png&s=4113)
响应式布局 Grid 组件
```javascript
import { sadColumn, sadRow, } from 'sadui'

<div style="width: 100%">
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
```
通过 span 属性设置跨度；
![sadGrid](https://user-gold-cdn.xitu.io/2020/3/15/170db83f9663afe8?w=1017&h=226&f=png&s=3530)
```javascript
<div style="width: 100%">
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
```
通过 gutter 属性设置边距
[!sadGrid](https://user-gold-cdn.xitu.io/2020/3/15/170db85bfd3ac3b8?w=1025&h=118&f=png&s=1937)
```javascript
<div style="width: 100%">
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
```
通过 offset 属性设置空白
## layout 布局
![sad-layout](https://user-gold-cdn.xitu.io/2020/3/15/170db891ffa6c4a9?w=697&h=190&f=png&s=2910)
```javascript
import { SadLayoutSider,SadLayoutFooter,SadLayoutHeader,SadLayout,SadLayoutContent, } from 'sadui'

<sad-layout>
  <sad-layout-header style="height: 50px; background:lightskyblue;">Header</sad-layout-header>
  <sad-layout-content style=" background:deepskyblue; color: black;">Content</sad-layout-content>
  <sad-layout-footer style="height: 50px; background:lightskyblue;">Footer</sad-layout-footer>
</sad-layout>
```
普通布局方案；
![sad-layout](https://user-gold-cdn.xitu.io/2020/3/15/170db8adab2643a5?w=716&h=178&f=png&s=3409)
```javascript
<sad-layout>
  <sad-layout-header style="height: 50px; background:lightskyblue;">Header</sad-layout-header>
  <sad-layout>
    <sad-layout-sider  style=" background:#ddd; color: black; width: 40px">Sider</sad-layout-sider>
    <sad-layout-content  style="background:deepskyblue">Content</sad-layout-content>
  </sad-layout>
  <sad-layout-footer style="height: 50px; background:lightskyblue;">Footer</sad-layout-footer>
</sad-layout>
```
带有 silder 的布局方案
## Toast 
![sad-toast](https://user-gold-cdn.xitu.io/2020/3/15/170db8d9373e097e?w=215&h=71&f=png&s=2620)
```javascript
import { plugin, sadButton } from 'sadui'
Vue.use(plugin)

<sad-button @click="$SadToast('点击弹出提示')" >Top</sad-button>
<sad-button @click="$SadToast('点击弹出提示', {position:'middle'})" >Middle</sad-button>
<sad-button @click="$SadToast('点击弹出提示', {position:'bottom'})" >Bottom</sad-button>
```
## 未完待续
