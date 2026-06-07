# 谢江铭 - 3D建模与渲染作品集网站

> 一个现代简约、响应式的个人作品集展示网站，专为3D建模师/渲染师设计。

## 🚀 快速开始

直接在浏览器中打开 `index.html` 即可预览网站，无需任何构建工具或服务器配置。

```bash
# 方式1：直接双击打开
双击 index.html

# 方式2：使用本地服务器（推荐，可解决跨域问题）
python -m http.server 8080
# 然后访问 http://localhost:8080
```

## 📁 网站结构

```
作品集/
├── index.html              # 主页面（包含所有HTML/CSS/JS）
├── README.md               # 本说明文件
├── 工作/                   # 项目图片素材目录
│   ├── 01.png ~ 26.png     # PBR模型/场景渲染图
│   ├── CT.png              # CT设备渲染图
│   ├── Product Shots*.png  # 产品拍摄图
│   └── ...                 # 其他项目图片
├── *.mp4                   # 动画视频文件
├── 相机*.jpg               # 相机产品图
└── 谢江铭图片作品集.pdf     # 原始作品集PDF
```

## 🎨 网站功能

| 功能 | 描述 |
|------|------|
| **作品集展示** | 18个精选项目，按5大类别（3D建模/Unity场景/产品渲染/动画视频/全景展厅）自动分类 |
| **分类筛选** | 点击顶部筛选按钮，按项目类型过滤显示 |
| **布局切换** | 支持网格布局和瀑布流布局两种展示模式 |
| **项目详情** | 点击卡片打开模态框，展示完整项目信息、图片画廊、视频演示和外部链接 |
| **灯箱查看** | 点击详情页图片可放大查看，支持键盘左右切换 |
| **深色/浅色模式** | 右上角一键切换，自动记忆用户偏好 |
| **响应式设计** | 完美适配桌面、平板和手机 |
| **联系表单** | 带前端验证的联系表单 |
| **滚动动画** | 元素进入视口时优雅的渐入动画 |
| **回到顶部** | 滚动超过600px后出现回到顶部按钮 |
| **平滑滚动** | 导航链接点击平滑滚动到对应区域 |

## ✏️ 如何修改内容

### 修改个人信息

在 `index.html` 中搜索以下位置修改：

- **姓名/简介**：搜索 `<h1>...谢江铭</h1>` 和 Hero 区域的描述文字
- **技能百分比**：搜索 `专业技能` 区域，修改 `style="width: 95%;"` 等数值
- **工作经历**：搜索 `工作经历` 区域
- **社交链接**：搜索 `fa-brands fa-github` 等图标附近的 `href="#"` 替换为你的链接
- **联系邮箱**：搜索 `jimikk@example.com`
- **页脚文字**：搜索 `2024 谢江铭`

### 添加新项目

在 `index.html` 的 `<script>` 标签内找到 `const projects = [` 数组，按以下格式添加：

```javascript
{
    id: 19,                          // 递增ID
    title: '你的项目标题',
    category: '3d-modeling',         // 分类：3d-modeling / unity-scene / product-rendering / animation / vr-exhibition
    tags: ['标签1', '标签2', '标签3'],
    cover: '工作/封面图.jpg',         // 卡片封面图路径（相对路径）
    images: ['工作/图1.jpg', '工作/图2.jpg'],  // 详情页图片画廊
    video: '视频.mp4',               // 可选，如有视频
    links: [                         // 可选，外部链接
        { label: '在线预览', url: 'https://example.com' }
    ],
    description: '简短描述（卡片上显示）',
    detail: '详细描述（详情页显示）',
    role: '你的角色',
    techs: ['技术1', '技术2'],
},
```

### 修改主题色

在 `<style>` 标签中的 Tailwind 配置里修改：

```javascript
colors: {
    primary: {
        500: '#06b6d4',  // 主色调 - 修改这个色值
        // ...
    },
}
```

## 🚢 部署网站

### 方式1：GitHub Pages（免费）

```bash
# 1. 将整个文件夹上传到 GitHub 仓库
git init
git add .
git commit -m "Initial portfolio"
git remote add origin https://github.com/你的用户名/你的仓库名.git
git push -u origin main

# 2. 在仓库 Settings > Pages 中启用 GitHub Pages
# 选择 main 分支，根目录，保存即可
```

### 方式2：Netlify（免费）

1. 注册 [Netlify](https://netlify.com)
2. 将文件夹拖拽到 Netlify 部署区域
3. 自动部署完成，获得 `xxx.netlify.app` 域名

### 方式3：任意静态服务器

将整个文件夹上传到任何支持静态文件的服务器即可，无需任何配置。

## 📋 技术栈

- **HTML5** - 语义化标签
- **Tailwind CSS v3** - 通过 CDN 加载的实用优先CSS框架
- **原生 JavaScript** - 无任何框架依赖
- **Font Awesome 6** - 图标库
- **Google Fonts (Inter)** - 字体

## 🔧 浏览器兼容性

| Chrome | Firefox | Safari | Edge |
|--------|---------|--------|------|
| ✅ 90+ | ✅ 90+ | ✅ 14+ | ✅ 90+ |

## 📝 许可

本项目为个人作品集展示用途。

---

**作者**: 谢江铭 (jimikk)  
**最后更新**: 2024年
