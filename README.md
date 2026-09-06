# Wanting Portfolio · 个人作品集网站

邓婉婷的 AI 产品经理个人作品集，Vue 3 + TypeScript + Vite 从零搭建。

**在线访问**：https://sinera-kiki.github.io/wanting/

## 页面结构

单页应用，共 8 个 section：

| Section | 内容 |
|---|---|
| Hero | 姓名 / Slogan / 求职方向 / 期望城市 / 简历下载 |
| About | 两面的我：专业 & 生活 |
| Experience | 实习经历时间线（小红书 / 杉数 / 科大讯飞 / 阿里巴巴），含核心指标 |
| Projects | 核心项目卡片（背景 / 动作 / 结果），含开源仓库入口 |
| Skills | 工具箱：AI 工程 / 产品设计 / 数据能力 / 工程基础 + 荣誉 |
| AI Projects | 独立 AI 项目（MeowLog 伴侣猫 / MealPlanner / AI 早报），含 Demo 与源码链接 |
| Creator | 内容创作与社会实践（小红书运营 / 校园推文 / 延安社会实践） |
| Beyond Work | 生活兴趣（王者荣耀 / 猫 / 小说 / 旅行 / 音乐）+ 家教经历 |
| Contact | 邮箱 / 微信 / 电话 / GitHub / 简历 PDF |

## 技术栈

- **Vue 3**（Composition API + `<script setup>`）
- **TypeScript**
- **Vite 5**
- **纯手写 CSS**：极简画廊风、莫兰迪绿主题、滚动淡入动画（IntersectionObserver，尊重 `prefers-reduced-motion`）、响应式适配

## 目录结构

```
├── src/
│   ├── pages/Home.vue        # 单页主组件（全部 section）
│   ├── composables/useReveal.ts  # 滚动进入视口动画
│   ├── styles.css            # 全局样式
│   └── assets/photos/        # 图片素材
├── public/                   # 简历 PDF、favicon
├── docs/                     # GitHub Pages 构建产物（自动生成，勿手改）
├── index.html
├── vite.config.ts
└── package.json
```

## 本地开发

```sh
npm install
npm run dev        # http://localhost:5173
```

## 构建与部署

```sh
npm run build          # 常规构建 → dist/
npm run build:pages    # GitHub Pages 构建 → docs/（自动加 /wanting/ 资源前缀）
```

将 `docs/` 提交到 `main` 分支即可，GitHub Pages 已配置为 **main 分支 /docs 目录** 托管。

## License

MIT © 2026 Deng Wanting
