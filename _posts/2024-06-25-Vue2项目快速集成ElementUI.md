---
layout: post

title: Vue2项目快速集成ElementUI

tag: Vue

typora-root-url: /images/posts
---

# 1、下载依赖

```shell
npm i element-ui -S
```

# 2、导入依赖

在`main.js`文件下添加如下代码即可

```javascript
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
Vue.use(ElementUI,{size:"small"});
```

# 3、测试

在任一`vue`文件中添加如下所示代码

```vue
<el-button>这是一个测试按钮</el-button>
```

效果如下所示

![1719581140412](/Vue/Quickly_integrate_ElementUI_into_a_Vue2_project/1719581140412.jpg)