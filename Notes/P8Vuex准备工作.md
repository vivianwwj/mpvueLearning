之前的数据获取：

数据存放于：app.js

通过：getApp获取

https://developers.weixin.qq.com/miniprogram/dev/reference/api/getApp.html



vuex用于管理vue状态

action和notation

```js
import Vue from 'vue'
import Vuex from 'vuex'
import store from './stroe'
import state from './state'
import actions from './actions'
import mutations from './mutations'
import getters from './getter'

// 声明使用vuex
Vue.use(Vuex)
  
//vue最核心的Store对象，需要暴露接口
export default new Vuex.Store({
  state,
  actions,
  getters,
  mutations
})
```

把store对象放到原型上

在入口文件main.js中进行放置

引入后放在原型上

需要在挂载前进行放置

```js
import store from './store/stroe'
//将store对象放置Vue的原型上，为的是每个实例都可以使用
Vue.prototype.$store = store
```