# Wanting Portfolio · 邓婉婷个人作品集

<div align="center">

[![Vue 3](https://img.shields.io/badge/Vue-3.4-4FC08D?style=flat-square&logo=vue.js&logoColor=white)](https://vuejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.4-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5.2-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev/)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-222222?style=flat-square&logo=github&logoColor=white)](https://sinera-kiki.github.io/wanting/)
[![License: MIT](https://img.shields.io/badge/License-MIT-8DA290?style=flat-square)](./LICENSE)

**面向 AI 产品经理 / AI Agent 独立开发岗位的个人求职作品集网站**

[🌐 在线访问 (Live Demo)](https://sinera-kiki.github.io/wanting/) · [📄 下载简历 (PDF)](https://sinera-kiki.github.io/wanting/wanting-deng-resume.pdf) · [🐙 GitHub 主页](https://github.com/Sinera-kiki)

</div>

---

## 💡 为什么从零自研这个网站？

作为一名**信息管理与信息系统**专业背景、主攻 **AI 产品经理** 与 **大模型 Agent 全栈落地** 的求职者，我希望通过一个完整可交互的 Web 产品来呈现自己的核心能力与审美：

- **左脑工程与数据**：具备 Python / TypeScript / SQL 动手能力，能独立跑通端到端 MVP 与复杂数据流；
- **右脑业务与共情**：深谙用户心理与 C 端网感，具备数万粉/万赞内容创作与深度调研经验。

网站采用 **Vue 3 + TypeScript + Vite** 从零架构，摒弃笨重 UI 框架，手写莫兰迪绿极简画廊风样式，追求极致加载性能与排版呼吸感。

---

## 🧭 页面模块导航

| 模块 | 锚点 | 核心内容 |
|---|---|---|
| **Hero 首页** | `#top` | 个人 Slogan、核心身份、求职方向、教育背景与简历下载直达 |
| **About 两面的我** | `#about` | 专业视角（代码/数据/业务）与生活视角（网感/共情/温度）的双栏对比 |
| **Experience 经历时间线** | `#experience` | 4 段实战经历（小红书治理 / 杉数科技 / 科大讯飞 / 阿里巴巴）与核心量化指标 |
| **Projects 核心业务项目** | `#projects` | 4 个业务落地项目（背景 / 动作 / 结果），含小红书治理开源代码入口 |
| **Skills 工具箱 & 荣誉** | `#skills` | AI 工程、产品设计、数据能力、工程基础 4 大技能矩阵与国家级/校级荣誉 |
| **AI Projects 独立全栈作品** | `#playground` | 独立 0→1 研发的 AI 产品（MeowLog 伴侣猫、MealPlanner 周餐助手、AI 早报推送） |
| **Creator 内容与社会实践** | `#creator` | 小红书千粉/万赞博主实战、校媒 50+ 篇深度推文、延安国家专项优秀社会实践 |
| **Beyond Work 生活另一面** | `#beyond` | 巅峰 2000 分王者辅助全局观、猫咪治愈、民谣文学、旅行观察与家教辅导经历 |
| **Contact 建立连接** | `#contact` | 邮箱、微信、电话、GitHub 与简历下载一键直达 |

---

## 🛠️ 技术栈与工程实践

### 前端技术栈
- **核心框架**：Vue 3 (`<script setup>` + Composition API)
- **类型系统**：TypeScript 5.4（严格类型推导，无 `any` 侵入）
- **路由管理**：Vue Router 4（轻量平滑滚动锚点支持）
- **构建工具**：Vite 5.2（基于 Rollup 的极致打包与 Tree-shaking）

### 性能与体验优化
1. **新一代图片格式（WebP）**：
   - 经过精细化有损/无损分级压缩，整站图片体积从原始 **19MB 骤降至 1.7MB**（瘦身 **91%**）。
   - 图片统一开启 `loading="lazy"` 懒加载，首屏头像采用 `fetchpriority="high"` 优先调度。
2. **零外部网络阻塞（自托管字体）**：
   - 将 Cormorant Garamond 与 Inter 字体（可变字体 woff2）完全内置在工程静态资源中，消除国内第三方 CDN 阻塞，实现零网络瀑布等待。
3. **极简轻量动效（IntersectionObserver）**：
   - 自主封装 `useReveal` composable，通过纯原生 `IntersectionObserver` 实现滚动渐入动效；
   - 严格遵循辅助功能无障碍标准，尊重用户操作系统的 `prefers-reduced-motion` 动效减弱偏好。
4. **全端响应式排版**：
   - 针对桌面大屏（1440px+）、笔记本（1024px）与移动端手机（375px~430px）逐一适配，支持横向滑动卡片与自适应流式网格。

---

## 📁 目录结构

```text
wanting/
├── docs/                     # GitHub Pages 部署目录（生产构建产物）
│   ├── assets/               # 哈希静态资源（JS/CSS/WebP/Woff2）
│   ├── favicon.jpg           # 站点图标
│   ├── wanting-deng-resume.pdf # 个人简历 PDF
│   ├── index.html            # 单页入口 HTML
│   └── .nojekyll             # 禁用 GitHub Pages Jekyll 构建
├── public/                   # 公共静态资源（开发与构建时原样复制）
│   ├── favicon.jpg
│   └── wanting-deng-resume.pdf
├── src/                      # 源码主目录
│   ├── assets/               # 静态资源与字体
│   │   ├── fonts/            # 自托管可变 woff2 字体
│   │   └── photos/           # 优化后的 WebP 摄影与项目截图
│   ├── components/           # 业务组件
│   │   └── NavBar.vue        # 顶部悬浮导航栏（滚动渐变与平滑锚点）
│   ├── composables/          # 组合式函数
│   │   └── useReveal.ts      # 原生滚动淡入动画监听
│   ├── pages/                # 页面视图
│   │   └── Home.vue          # 单页主体（全模块数据驱动与响应式布局）
│   ├── App.vue               # 根组件（全局布局与页脚）
│   ├── main.ts               # 应用入口（路由与挂载）
│   ├── styles.css            # 全局样式系统（CSS 变量、排版、动效）
│   └── vite-env.d.ts         # Vite 与静态模块类型声明
├── .gitignore                # Git 忽略配置
├── index.html                # Vite 模板入口
├── package.json              # 依赖与脚本配置
├── tsconfig.json             # TypeScript 编译器配置
├── vite.config.ts            # Vite 构建配置
├── LICENSE                   # MIT 开源许可证
└── README.md                 # 项目详细文档
```

---

## 💻 本地运行与构建

### 1. 环境准备
- Node.js >= 18.0.0
- npm >= 9.0.0

### 2. 安装依赖
```bash
git clone https://github.com/Sinera-kiki/wanting.git
cd wanting
npm install
```

### 3. 启动本地开发服务
```bash
npm run dev
# 本地访问：http://localhost:5173
```

### 4. 静态类型检查
```bash
npm run typecheck
```

### 5. 生产构建与 GitHub Pages 部署
```bash
# 1. 执行 Pages 自动化构建（输出至 docs/ 目录）
npm run build:pages

# 2. 提交并推送到 GitHub main 分支
git add .
git commit -m "feat: update portfolio content"
git push origin main
```

---

## 📬 关于作者

- **姓名**：邓婉婷 (Wanting Deng)
- **教育背景**：东南大学 (985) · 信息管理与信息系统
- **求职方向**：AI 产品经理 / 大模型应用 / AI Agent 全栈落地
- **个人邮箱**：dwt15229556298@163.com
- **工作邮箱**：dengwanting@xiaohongshu.com
- **微信**：15229556298
- **GitHub**：[@Sinera-kiki](https://github.com/Sinera-kiki)

---

<div align="center">

*© 2026 Wanting Deng · Made with quiet care*

</div>
