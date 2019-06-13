# 《HelloGitHub》第 27 期
>兴趣是最好的老师，**HelloGitHub** 就是帮你找到兴趣！
<p align="center">
    <img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/01/img/hello-github.jpg' style="max-width:100%;"></img>
</p>

## 简介
分享 GitHub 上有趣、入门级的开源项目。

这是一个面向**编程新手**、**热爱编程**、**对开源社区感兴趣** 人群的月刊，月刊的内容包括：**各种编程语言的项目**、**让生活变得更美好的工具**、**书籍、学习笔记、教程等**，这些开源项目大多都是非常容易上手，而且非常 Cool。主要是希望大家能动手用起来，加入到**开源社区**中。
- 会编程的可以贡献代码
- 不会编程的可以反馈使用这些工具中的 Bug
- 帮着宣传你觉得优秀的项目
- Star 项目⭐️

在浏览、参与这些项目的过程中，你将学习到**更多编程知识**、**提高编程技巧**、**找到编程的乐趣**。

🎉 最后 [HelloGitHub](https://hellogithub.com) 这个项目就诞生了 🎉

---
> **以下为本期内容**｜每个月 **28** 号发布最新一期｜[点击查看往期内容](https://github.com/521xueweihan/HelloGitHub#内容)

#### C# 项目
1、[Rosin](https://github.com/AlloyTeam/Rosin)：一个 Fiddler 插件，用于协助开发者进行移动端页面开发、调试

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/Rosin-min.jpeg' style="max-width:80%; max-height=80%;"></img></p>

2、[SiteServer-CMS](https://github.com/siteserver/cms/)：开源、免费、企业级内容管理平台。基于该工具可以快速、方便地搭建搭建一个性能优异、颇具规模、易于维护的网站平台

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/SiteServer-CMS-min.png' style="max-width:80%; max-height=80%;"></img></p>

#### C++ 项目
3、[MyTinySTL](https://github.com/Alinshans/MyTinySTL)：用 C++11 实现的小型 STL（容器库＋算法库）。代码结构清晰规范、包含中文文档与注释，并且自带一个简单的测试框架，适合新手学习与参考。示例代码如下：
```c++
// 在尾部插入元素
template <class T>
void vector<T>::push_back(const value_type& value)
{
  if (end_ != cap_)
  {
    data_allocator::construct(mystl::address_of(*end_), value);
    ++end_;
  }
  else
  {
    reallocate_insert(end_, value);
  }
}
```

#### Go 项目
4、[appify](https://github.com/machinebox/appify)：该项目能够方便的把 Golang 项目包装成 MacOS 可以直接运行的软件。可以用来把自己写的小工具包装成一个其他人可以直接下载并双击使用的软件。提供自定义 logo、名字，分分钟发布自己的 Golang 软件。使用步骤如下：
```shell
# 1.安装命令
$ go get github.com/machinebox/appify

# 2.封装命令
$ appify -name "My Go Application" -icon ./icon.png /path/to/bin
```

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/appify-min.png' style="max-width:80%; max-height=80%;"></img></p>

5、[usql](https://github.com/xo/usql)：通用SQL命令行客户端。支持以下所有数据库和协议：

| 数据库 (scheme/driver)        | 协议别名 [real driver]                 |
|------------------------------|---------------------------------------|
| Microsoft SQL Server (mssql) | ms, sqlserver                         |
| MySQL (mysql)                | my, mariadb, maria, percona, aurora   |
| Oracle (ora)                 | or, oracle, oci8, oci                 |
| PostgreSQL (postgres)        | pg, postgresql, pgsql                 |
| SQLite3 (sqlite3)            | sq, sqlite, file                      |

```
安装方法
1. 根据你的系统下载最新的 binary
2. 解压缩出 `usql` 或者 `usql.exe`
3. 把binary放到你的 `$PATH` (Linux/macOS) 或 `%PATH%` (Windows)路径下
4. 然后就可以用`usql`链接到你喜欢的SQL数据库啦~
```

#### Java 项目
6、[RetrofitUrlManager](https://github.com/JessYanCoding/RetrofitUrlManager)：以简洁的 API 让 Retrofit 同时支持多个 BaseUrl，动态改变 BaseUrl

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/RetrofitUrlManager.gif' style="max-width:80%; max-height=80%;"></img></p>

#### JavaScript 项目
7、[v-region](https://github.com/TerryZ/v-region)：使用 Vue 创建的中国省市区选择组件，组件复用程度高、可直接引入项目中使用。使用场景适用于需要用户选择地址，采用该组件可以提高交互程度。[文档](https://terryz.github.io/vue/#/region/demo)，示例代码：
```js
<v-region :city="false" :area="false" class="form-control"></v-region> // 只显示省份
<v-region :area="false" class="form-control"></v-region> // 显示省市
<v-region class="form-control"></v-region> // 显示省市区
```

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/v-region-min.png' style="max-width:80%; max-height=80%;"></img></p>

8、[whistle](https://github.com/avwo/whistle)：基于 Node.js 实现的跨平台 web 调试代理工具，类似于 Windows 平台上的 Fiddler。主要用于查看、修改HTTP、HTTPS、Websocket的请求、响应，也可以作为 HTTP 代理服务器使用。不同于 Fiddler 通过断点修改请求响应的方式，whistle 采用的是类似配置系统 hosts 的方式，一切操作都可以通过配置实现。通过该工具，可以现实复杂的前端环境、生产、开发、bugFix 一键切换。

9、[simpread](https://github.com/Kenshin/simpread)：让你瞬间进入沉浸式阅读的扩展，还原阅读的本质，提升你的阅读体验。使用它可以为你剔除页面上无关的干扰信息，让用户专注于阅读主要的内容。通过这个项目，还可以学习如何开发 Chrome 扩展

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/simpread-min.png' style="max-width:80%; max-height=80%;"></img></p>

10、[incubator-echarts](https://github.com/apache/incubator-echarts)：使用 JavaScript 实现的开源、流行、强大的可视化库。可以流畅的运行在 PC 和移动设备上，兼容当前绝大部分浏览器。提供直观、交互丰富、可实现高度个性定制化的数据可视化图表，也可将其封装为任何 MVVM 框架的组件方便适用。[官网](http://echarts.baidu.com/)

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/incubator-echarts-min.png' style="max-width:80%; max-height=80%;"></img></p>

#### Objective-C 项目
11、[KafkaRefresh](https://github.com/OpenFeyn/KafkaRefresh)：内置多种动画、可自定义和灵活的 iOS 下拉刷新框架。[中文文档](https://github.com/OpenFeyn/KafkaRefresh/blob/master/CREADME.md)

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/KafkaRefresh.gif' style="max-width:80%; max-height=80%;"></img></p>

#### Python 项目
12、[tenacity](https://github.com/jd/tenacity)：使用该库可以优雅地实现各种需求的重试。示例代码如下：
```python
from tenacity import retry, stop_after_attempt

# 通过装饰器，实现遇到异常重试3次
@retry(stop=stop_after_attempt(3)) 
def get_data(url):
    response = requests.get(url)
    response_json = response.json()
```

13、[unimatrix](https://github.com/will8211/unimatrix)：模拟“黑客帝国”影片中的终端动画脚本

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/unimatrix-min.png' style="max-width:80%; max-height=80%;"></img></p>

14、[pudb](https://github.com/inducer/pudb)：基于控制台的全屏 Python 可视化调试器。比 pdb 好用太多了，特性：
- 源码语法高亮，栈、断点、变量可见并且一直动态更新。变量展示还有很多可以定制化的功能。
- 基于键盘，简单高效。支持 VI 的鼠标移动。还支持 PDB 的某些命令
- 支持查找源代码，可以使用 m 代用 module browser 查看载入的模块
- 断点设置。鼠标移到某行代码，按 b，然后可以在断点窗口编辑断点

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/pudb-min.png' style="max-width:80%; max-height=80%;"></img></p>

#### Ruby 项目
15、[hacker101](https://github.com/Hacker0x01/hacker101)：（英文）一个免费的 Web安全课程。无论你是一个程序员、对 bug 悬赏感兴趣，或是一个经验丰富的安全专业人员，在 HACKE101 课程中都可以学到东西。包涵大量示例代码和在线 Demo，示例代码为 Ruby。

#### Swift 项目
16、[IBAnimatable](https://github.com/IBAnimatable/IBAnimatable)：一个帮助我们在 Interface Builder 和 Swift Playground 里面设计 UI、交互、导航模式,、换场和动画的开源库。下图的整个 App 都是通过 IBAnimatable 在 Interface Builder 设计完成，没有任何一行代码。

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/IBAnimatable.gif' style="max-width:80%; max-height=80%;"></img></p>

17、[TuringCalendar](https://github.com/zhihaozhang/TuringCalendar)：图灵教育推出的限量款[编程日历 2018](http://www.ituring.com.cn/book/download/43507086-33c3-40e9-9115-d610e1333bca)，因为简约大气的设计和每周一个编程语言的介绍，在程序员中广受欢迎。现在日历 PDF 的源文件已经开源，于是就有了这个项目。一个 macOS 桌面上的日历 widget，效果图如下：

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/TuringCalendar-min.jpeg' style="max-width:80%; max-height=80%;"></img></p>

#### 其它
18、[project-guidelines](https://github.com/elsewhencode/project-guidelines)：JavaScript 工程项目的一系列最佳实践策略，[中文版](https://github.com/elsewhencode/project-guidelines/blob/master/README-zh.md)。其它编程语言的项目也有可以借鉴的地方

19、[Android_Data](https://github.com/Freelander/Android_Data)：这个集合主要能够帮助初学者在初学 Android 开发的时候，能够快速、方便地找到适合自己的学习资料

20、[Front-End-Checklist](https://github.com/thedaviddias/Front-End-Checklist)：一份在网站发布到生产环境之前，前端部分需要测试、检查的详尽清单。[中文版](https://github.com/JohnsenZhou/Front-End-Checklist)

21、[build-your-own-x](https://github.com/danistefanovic/build-your-own-x)：（英文）费曼：“我不能创造的東西，我就不了解。”该项目收集了不同编程语言造轮子的教程

#### 机器学习
22、[simplified-deeplearning](https://github.com/exacity/simplified-deeplearning)：《DeepLearningBook》读书笔记

23、[elasticsearch-spark-recommender](https://github.com/IBM/elasticsearch-spark-recommender)：使用 Apache Spark 的机器学习库 (MLlib) 来训练一个协同过滤推荐系统模型 和 Elasticsearch 构建一个推荐系统教程，[中文版阅读](https://github.com/IBM/elasticsearch-spark-recommender/blob/master/README-cn.md)

<p align="center"><img src='https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/27/img/elasticsearch-spark-recommender-min.png' style="max-width:80%; max-height=80%;"></img></p>



---
<p align="center">
    “看完了，还不够？<a href='https://github.com/521xueweihan/HelloGitHub#%E5%86%85%E5%AE%B9'><往期内容></a> | 还不过瘾，那就看看每天更新的前端日报吧 <a href='https://daily.fairyever.com/'><今日前端></a>”<br>
    如果你发现了好玩、有意义的开源项目 <a href='https://github.com/521xueweihan/HelloGitHub/issues/new'>点击这里</a> 分享你觉得有趣的项目。
</p>

## 公众号
最近开了公众号，后续公众号会针对月刊推荐过的内容精选、梳理，做成系列的文章发布。月刊也会同时发布在公众号，便于第一时间阅读。

<p align="center">
  <img src="https://raw.githubusercontent.com/521xueweihan/img/master/hellogithub/logo/weixin.png" style="max-width:70%;"></img><br>
欢迎关注 HelloGitHub 公众号，获取更多开源项目的资料和内容。
</p>

## 声明
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">知识共享署名-相同方式共享 4.0 国际许可协议</a>进行许可。

**欢迎转载，请注明出处和作者，同时保留声明。**
