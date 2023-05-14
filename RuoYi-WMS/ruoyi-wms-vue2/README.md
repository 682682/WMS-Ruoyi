## 开发

```bash
# 安装依赖
npm install

# 建议不要直接使用 cnpm 安装依赖，会有各种诡异的 bug。可以通过如下操作解决 npm 下载速度慢的问题
npm install --registry=https://registry.npmmirror.com

# 启动服务
npm run dev
```

## 发布

```bash
# 构建测试环境
npm run build:stage

# 构建生产环境
npm run build:prod
```
## 后端开源项目地址
### gitee
https://gitee.com/zccbbg/wms-ruoyi
### github
https://github.com/zccbbg/wms-ruoyi

## 在线体验
- 演示地址：http://wms.ichengle.top
- 陆陆续续收到一些打赏，为了更好的体验已用于演示服务器升级。谢谢各位小伙伴。

## 若依wms简介
若依wms是一套基于若依的wms仓库管理系统，支持lodop和网页打印入库单、出库单。毫无保留给个人及企业免费使用。
* 前端采用Vue、Element UI（ant design 正在开发中）。
* 后端采用Spring Boot、Spring Security、Redis & Jwt。
* 权限认证使用Jwt，支持多终端认证系统。
* 支持加载动态权限菜单，多方式轻松权限控制。
* 高效率开发，使用代码生成器可以一键生成前后端代码。

## 若依wms功能
1. 首页：库存预警与到期提醒、基础数据报表展示
2. 仓库/库区/货架：管理维护仓库基础数据
3. 物料：管理维护物料基础数据
4. 客户/供应商/承运商：管理维护联系人基础数据
5. 入库：创建入库单后包括如下几个状态：未发货、在途（已发货未入库）、部分入库、作废、入库完成，入库类型包括：采购入库、外协入库、退货入库，入库单支持lodop和网页打印
6. 出库：创建出库单后包括如下几个状态：未发货、部分发货、已发货、作废，入库类型包括：销售出库、外协出库、调拨出库，出库单支持lodop和网页打印
7. 移库：创建移库单后包括如下几个状态：未操作、部分移动、操作完毕、作废
8. 库存看板：查看当前物料库存数量
9. 库存记录：查看当前物料库存操作记录
## 状态流转
#### 入库状态流转
![入库状态流转](https://oscimg.oschina.net/oscnet/up-6bdb5ad6d8ab236f763300b71cf175d9a99.jpg)
#### 出库状态流转
![出库状态流转](https://oscimg.oschina.net/oscnet/up-55cad3f077f914e357efeaae0b3feecf942.jpg)

## 关于我们
开发团队成立5年，我们前端开发、后端架构，有一颗热爱开源的心，致力于打造企业级的通用产品设计UI体系让项目 或者更直观，更高效、更简单，未来将持续关注UI交互，持续推出高质量的交互产品。

## 演示图
![首页](https://oscimg.oschina.net/oscnet/up-89f751967b4145f7da92e23536bf231fbe8.jpg)
![支持两种打印方式](https://oscimg.oschina.net/oscnet/up-6daf90ef19571c7f0e7641ae59c403d8272.jpg)
![lodop打印](https://oscimg.oschina.net/oscnet/up-146d2105ae31a27e497323ad19f8bd0d7bd.jpg)
![网页打印](https://oscimg.oschina.net/oscnet/up-5664440042861199d1f3e60928e0700a9ce.jpg)
![仓库列表](https://oscimg.oschina.net/oscnet/up-a00eb79bee48e481249a12cb5e6c476aaa3.jpg)
![库存看板](https://oscimg.oschina.net/oscnet/up-78990915dfba902384ed4b09e3dc0f0fe05.jpg)

## 若依内置功能

1.  用户管理：用户是系统操作者，该功能主要完成系统用户配置。
2.  部门管理：配置系统组织机构（公司、部门、小组），树结构展现支持数据权限。
3.  岗位管理：配置系统用户所属担任职务。
4.  菜单管理：配置系统菜单，操作权限，按钮权限标识等。
5.  角色管理：角色菜单权限分配、设置角色按机构进行数据范围权限划分。
6.  字典管理：对系统中经常使用的一些较为固定的数据进行维护。
7.  参数管理：对系统动态配置常用参数。
8.  通知公告：系统通知公告信息发布维护。
9.  操作日志：系统正常操作日志记录和查询；系统异常信息日志记录和查询。
10. 登录日志：系统登录日志记录查询包含登录异常。
11. 在线用户：当前系统中活跃用户状态监控。
12. 定时任务：在线（添加、修改、删除)任务调度包含执行结果日志。
13. 代码生成：前后端代码的生成（java、html、xml、sql）支持CRUD下载 。
14. 系统接口：根据业务代码自动生成相关的api接口文档。
15. 服务监控：监视当前系统CPU、内存、磁盘、堆栈等相关信息。
16. 缓存监控：对系统的缓存信息查询，命令统计等。
17. 在线构建器：拖动表单元素生成相应的HTML代码。
18. 连接池监视：监视当前系统数据库连接池状态，可进行分析SQL找出系统性能瓶颈。
<table>
    <tr>
        <td><img src="https://oscimg.oschina.net/oscnet/cd1f90be5f2684f4560c9519c0f2a232ee8.jpg"/></td>
        <td><img src="https://oscimg.oschina.net/oscnet/1cbcf0e6f257c7d3a063c0e3f2ff989e4b3.jpg"/></td>
    </tr>
    <tr>
        <td><img src="https://oscimg.oschina.net/oscnet/up-8074972883b5ba0622e13246738ebba237a.png"/></td>
        <td><img src="https://oscimg.oschina.net/oscnet/up-9f88719cdfca9af2e58b352a20e23d43b12.png"/></td>
    </tr>
    <tr>
        <td><img src="https://oscimg.oschina.net/oscnet/up-39bf2584ec3a529b0d5a3b70d15c9b37646.png"/></td>
        <td><img src="https://oscimg.oschina.net/oscnet/up-936ec82d1f4872e1bc980927654b6007307.png"/></td>
    </tr>
	<tr>
        <td><img src="https://oscimg.oschina.net/oscnet/up-b2d62ceb95d2dd9b3fbe157bb70d26001e9.png"/></td>
        <td><img src="https://oscimg.oschina.net/oscnet/up-d67451d308b7a79ad6819723396f7c3d77a.png"/></td>
    </tr>	 
    <tr>
        <td><img src="https://oscimg.oschina.net/oscnet/5e8c387724954459291aafd5eb52b456f53.jpg"/></td>
        <td><img src="https://oscimg.oschina.net/oscnet/644e78da53c2e92a95dfda4f76e6d117c4b.jpg"/></td>
    </tr>
	<tr>
        <td><img src="https://oscimg.oschina.net/oscnet/up-8370a0d02977eebf6dbf854c8450293c937.png"/></td>
        <td><img src="https://oscimg.oschina.net/oscnet/up-49003ed83f60f633e7153609a53a2b644f7.png"/></td>
    </tr>
	<tr>
        <td><img src="https://oscimg.oschina.net/oscnet/up-d4fe726319ece268d4746602c39cffc0621.png"/></td>
        <td><img src="https://oscimg.oschina.net/oscnet/up-c195234bbcd30be6927f037a6755e6ab69c.png"/></td>
    </tr>
    <tr>
        <td><img src="https://oscimg.oschina.net/oscnet/b6115bc8c31de52951982e509930b20684a.jpg"/></td>
        <td><img src="https://oscimg.oschina.net/oscnet/up-5e4daac0bb59612c5038448acbcef235e3a.png"/></td>
    </tr>
</table>


## 关于我们
* 开发团队成立5年，我们前端开发、后端架构，有一颗热爱开源的心，致力于打造企业级的通用产品设计UI体系让项目 或者更直观，更高效、更简单，未来将持续关注UI交互，持续推出高质量的交互产品。
* 这五年我主要做isv对接淘宝、拼多多、抖音、美团等平台的订单处理应用，日处理订单300w条，因为要熟悉业务也开过淘宝和拼多多店铺运营了一个网易严选的品牌。我们的公众号会陆续更新一些我一边撸代码一边做客服的经历。也会更新一些我的读书笔记以及编程、创业、生活中踩坑的文章。另外还会开放一些米哈游、博世、企查查、同程、阿里、京东、拼多多等大厂、中厂或外企的内推岗位！
* 交流合作可加微信：zccbbg

## 交流群

|                          [点击加入qq群](https://jq.qq.com/?_wv=1027&k=u59FVnYG)                           |
|:--------------------------------------------------------------:|
|           <img src="doc/qqgroup.jpg" width="200px">            | 

|              微信群： 关注公众号，回复：加群     |
|:------------------------------------------:|
| <img src="doc/datacall.jpg" width="200px"> | 

## 大厂、外企内推
关注“字节叔叔”公众号：记录编程、创业、生活中踩坑的文章，陆续会开放一些微软、阿里、京东、拼多多等大厂或外企的内推岗位！