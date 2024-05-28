# 个人音乐播放器
## login：
登录表单输入验证，规范表单数据，防止xss攻击，登录成功后跳转首页，同时同步个人信息姓名等到vuex的store仓库中，还有微信登录接口
##### form表单验证、vuex数据管理、uni路由跳转、数据双向绑定同步、uni微信登陆接口

## index:
调用时间戳获取当前时间，并根据时间调整首页问候语，
中间区域为土味情话api数据，可以替换为音乐资讯，
推送三条人气较高音乐在首页，下方听歌打卡模块调用uni日历组件也可以当日历工具使用
#### api接口调用、uni媒体组件、生命周期钩子函数、封装信息渲染方法xuanran.js

## list：
获取仓库中的歌曲列表渲染到页面中展示，使用uni组件分页器，编写对应方法与列表结合渲染
头部搜索框可以搜索歌手名字查看歌曲列表中的对应数据，支持模糊搜索
播放音乐会添加到最近播放列表、关联对应数据
#### vuex数据管理、uni组件、逻辑处理、数据关联、封装音乐播放方法startSong.js、封装列表渲染方法uselist.js、computed计算属性

## about：
关于我们页面，从仓库中获取歌手信息，使用uni九宫格组件渲染数据，点击跳转歌手详情页
点击对应歌手会传递歌手参数显示歌曲列表中对应数据
左下角小组件可以作为扩展功能使用
#### uni数据渲染组件、路由跳转、组件封装、组件嵌套

## user：
登陆后user页面自动获取store仓库中相关数据，并根据username做出判断渲染头像显示
修改对应name头像也会对应改变并同步渲染首页数据
菜单中收藏、喜欢、已购、最近播放音乐分别获取数据渲染
退出登录后清空相关缓存数据跳转登录页面
#### uni dialog对话框组件、定时器、组件封装使用、watch监听属性、生命周期钩子函数

## songDetail:
显示当前播放的音乐信息，添加唱片动画
进度条同步歌曲播放进度，通过进度条控制播放进度
组件控制音乐播放，新增收藏、喜欢功能
#### innerAudioContext对象属性及其方法使用
