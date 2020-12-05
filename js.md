# js
- 事件运行机制【JavaScript引擎的内部运行机制】
http://www.ruanyifeng.com/blog/2014/10/event-loop.html

    ```
    JavaScript语言的一大特点就是单线程，也就是说，同一个时间只能做一件事
     1）所有同步任务都在主线程上执行，形成一个执行栈（execution context stack）。

    （2）主线程之外，还存在一个"任务队列"（task queue）。只要异步任务有了运行结果，就在"任务队列"之中放置一个事件。

    （3）一旦"执行栈"中的所有同步任务执行完毕，系统就会读取"任务队列"，看看里面有哪些事件。那些对应的异步任务，于是结束等待状态，进入执行栈，开始执行。

    （4）主线程不断重复上面的第三步。
    ```
- vue 
    ```
    vue --version:查看vue版本
    ```
-   `vue create hello-world`：创建项目，hello-world项目名称

# npm

- `npm install -g npm@latest` ：npm 安装到最新版本

- `npm install -g cnpm --registry=https://registry.npm.taobao.org`:切换到淘宝镜像