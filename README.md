#### 介绍
React Ant Admin

#### 规划

- 从零使用 `react` 搭建系统
- 全面使用 `react-hooks` 开发，抛弃 `class` 组件写法、所有组件异步加载，提高首屏渲染速度
- 动态权限设计，开发配套的后端 Api
- ...

#### 使用技术

- **UI 框架**: `react`、`react-hook`、`classnames`
- **UI 组件**: `antd`、`@ant-design/aliyun-theme`
- **数据管理**：`redux`、`react-redux`、`redux-thunk`、`redux-logger`
- **类型检查**：`typescript`
- **接口请求**：`axios`
- **cookies**：`js-cookie`
- **过渡动画**：`react-transition-group`
- **CSS 规则**：`BEM`

#### 菜单

```js
-首页介绍 - 系统介绍 - 权限管理 - 用户管理 - 角色管理 - 菜单管理;
```

#### 使用

```bash
$ npm install
$ npm start

```

#### 文件说明

```js
.
├── README.md
├── package-lock.json
├── package.json
├── src
│   ├── App.test.tsx
│   ├── App.tsx
│   ├── api
│   │   ├── request.ts // Axios 请求统一封装
│   │   └── requestMd.ts // md 单独使用的 axios 实例
│   ├── components // 系统组建和业务无关
│   │   ├── Breadcrumb // 面包屑导航
│   │   │   ├── index.less
│   │   │   └── index.tsx
│   │   ├── Hamburger // 菜单栏开关
│   │   │   ├── index.less
│   │   │   └── index.tsx
│   │   ├── HeaderSearch // 头部搜索
│   │   │   └── index.tsx
│   │   ├── LayoutHeader // 系统头部
│   │   │   ├── index.less
│   │   │   └── index.tsx
│   │   ├── LayoutNavBar // 系统头部右侧内容
│   │   │   ├── AvatarDropdown.tsx
│   │   │   ├── NavBarItem.tsx
│   │   │   ├── NavDropdown.tsx
│   │   │   ├── index.less
│   │   │   └── index.tsx
│   │   ├── LayoutSettings // 系统设置
│   │   │   ├── index.less
│   │   │   └── index.tsx
│   │   ├── LayoutSideBar // 侧边栏导航
│   │   │   ├── index.less
│   │   │   └── index.tsx
│   │   ├── NoticeIcon // 消息通知
│   │   │   ├── NoticeTab.less
│   │   │   ├── NoticeTab.tsx
│   │   │   ├── index.less
│   │   │   └── index.tsx
│   │   ├── SideMenu // 菜单栏
│   │   │   ├── index.less
│   │   │   └── index.tsx
│   │   ├── SidebarLogo // 菜单栏logo
│   │   │   ├── index.less
│   │   │   └── index.tsx
│   │   └── TransitionMain // 主体内容过度
│   │       └── index.tsx
│   ├── hooks // 自定义 react-hook
│   │   └── count.ts
│   ├── index.tsx
│   ├── layout
│   │   ├── AsyncRoutes.tsx // 负责异步路由请求和渲染
│   │   ├── Auth.tsx  // 权限校验
│   │   ├── MainRoutes.tsx // 业务路由渲染
│   │   ├── UserLayout.less // 系统用户路由渲染
│   │   ├── UserLayout.tsx
│   │   ├── index.less
│   │   └── index.tsx // 系统主要layout
│   ├── react-app-env.d.ts
│   ├── router
│   │   ├── config.ts // 项目的路由配置
│   │   └── utils.ts // 路由相关的一些 utils
│   ├── serviceWorker.ts
│   ├── store  // redux
│   │   ├── index.ts
│   │   ├── module
│   │   │   ├── app.ts
│   │   │   ├── notice.ts
│   │   │   ├── settings.ts
│   │   │   └── user.ts
│   │   └── types.ts
│   ├── styles // 基本公用的样式
│   │   ├── index.less
│   │   ├── md.css
│   │   └── var.less
│   ├── typings // 类型申明
│   │   ├── global.d.ts
│   │   └── index.ts
│   ├── utils // 工具类
│   │   ├── cookie.ts
│   │   ├── store.ts
│   │   └── verifty.ts
│   └── views // 视图
│       ├── auth
│       │   ├── menu
│       │   │   ├── AddOrEditMenu.tsx
│       │   │   ├── index.tsx
│       │   │   └── service.ts
│       │   ├── role
│       │   │   ├── AddOrEdit.tsx
│       │   │   ├── editMenu.tsx
│       │   │   ├── index.tsx
│       │   │   └── service.ts
│       │   └── user
│       │       ├── AddOrEdit.tsx
│       │       ├── index.tsx
│       │       └── service.ts
│       ├── components
│       │   ├── BaseTable.tsx
│       │   ├── PageWrap.tsx
│       │   ├── SearchForm.tsx
│       │   └── index.less
│       ├── dashborad
│       │   └── intro
│       │       ├── index.tsx
│       │       └── intro.md
│       ├── error
│       │   ├── 403.tsx
│       │   └── 404.tsx
│       └── system
│           ├── component
│           │   ├── FormItem.tsx
│           │   ├── FormWrap.tsx
│           │   └── LoginItem.tsx
│           ├── login
│           │   ├── index.less
│           │   ├── index.tsx
│           │   └── service.ts
│           ├── recoveryPwd
│           │   ├── index.tsx
│           │   └── service.ts
│           ├── register
│           │   ├── index.tsx
│           │   └── service.ts
│           └── registerResult
│               └── index.tsx
└── tsconfig.json
