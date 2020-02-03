# 前端自动化测试 jest

## 为什么要去学习自动化测试？
1. 减少代码bug率，代码更健壮，组织逻辑性更好
2. 长期迭代更新的代码更易维护
3. 防止修改其他人或者时间过久的时项目，修改一处，引出其他问题
4. 点亮自身技能，开阔自己的知识面

[![1579489806.jpg](https://i.postimg.cc/K8mzY4bc/1579489806.jpg)](https://postimg.cc/ykrBQ1W2)

## 在实际项目中运用jest所具备知识点
1. jest （测试框架）
* 匹配器matchers  
https://blog.csdn.net/Jsoning/article/details/103898385
* 钩子函数  
https://blog.csdn.net/Jsoning/article/details/103984393
* 异步代码测试  
https://blog.csdn.net/Jsoning/article/details/103976195
* mock 函数  
https://blog.csdn.net/Jsoning/article/details/103992103
* 定时器测试  
https://blog.csdn.net/Jsoning/article/details/104014997
* snapshot快照测试  
https://blog.csdn.net/Jsoning/article/details/104015027
* TDD、BDD、单元测试、集成测试（简单了解）  
https://blog.csdn.net/Jsoning/article/details/104015061

以上链接是对于各个知识点用法的个人总结，包括了大部分jest框架中的用法，当然也可以去查看jest的官方文档

2. Vue Test Utils （ Vue.js官方的单元测试实用工具库）
* 想要在vue中更方便的使用jest进行测试的话，vue官方很贴心的提供了一个test-utils，可以更方便的对vue中的组件，DOM等进行测试
* 官网链接：https://vue-test-utils.vuejs.org/zh/

3. vuejs
* 想要在vue中使用jest，对于vue框架的熟练使用是必备的


## 在vue中使用jest

**<font color=red>前提已经了解以上3点基础知识</font>**  

这里做了一个demo，大致先了解一下demo所具有的功能
[![11.gif](https://i.postimg.cc/DzDmDmwG/11.gif)](https://postimg.cc/wtX6RqJx)

这个demo涉及到的测试功能有：
* DOM的测试
* 异步代码测试
* 定时器测试
* vuex测试
* 快照测试
* 单元测试
* 集成测试
* 等

**下面我们开始分析项目demo**  
1. 安装jest  
在通过`vue-cli`初始化项目的时候，选择单元测试和jest测试框架即可

2. 项目结构  
[![1.png](https://i.postimg.cc/SKrXm8pY/1.png)](https://postimg.cc/McnZDnHz)
* 这里默认初始化完项目后，`tests`是一个单独的文件夹，如果将所有的测试文件都写在一个文件中，当你找一个测试文件时候比较麻烦。这里我将每个组件文件夹下都添加一个`tests`文件夹，这样项目结构使用起来更方便
* 因为修改了测试文件的目录，因此需要重新在`jest.config.js`配置一下jest检查测试文件的查找路径(更多配置可以查看官网：https://jestjs.io/docs/en/configuration)
[![2.png](https://i.postimg.cc/hPCvZxq2/2.png)](https://postimg.cc/ppFPpmrj)
* 脚手架默认是查找`xx.spec.js`测试文件，刚才修改路径的时候我们保留了默认配置




