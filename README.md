# 师鑫荣 - 个人网站

一个现代化的个人简历网站，采用 Next.js + TypeScript + Tailwind CSS + Framer Motion 构建。

## 功能特点

### 🎨 视觉设计
- **玻璃拟态效果 (Glassmorphism)**：所有卡片使用半透明磨砂效果
- **星空背景**：动态的星星动画背景
- **渐变文字**：使用紫色到粉色的渐变文字效果
- **滚动动画**：内容逐行浮现的动画效果

### 📱 页面结构
1. **引导页**：极简设计，展示姓名、职位和个人自述
2. **全量简历页**：
   - 侧边栏导航（星光导航条）
   - 可折叠卡片（Accordion）
   - 网格布局展示课程设计
   - 模态框显示详细信息

### 🎯 交互特性
- **分段加载**：内容按需显示，提升性能
- **平滑滚动**：点击导航平滑跳转到对应区域
- **响应式设计**：完美适配桌面端和移动端
- **悬停效果**：卡片悬停时的动画反馈

### 🤖 AI 助手集成
- 完整的简历数据注入到 System Prompt
- 支持基于简历数据的智能问答
- 可扩展的 API 接口设计

## 技术栈

- **框架**: Next.js 14 (App Router)
- **语言**: TypeScript
- **样式**: Tailwind CSS
- **动画**: Framer Motion
- **图标**: Lucide React

## 快速开始

### 安装依赖

\`\`\`bash
npm install
\`\`\`

### 运行开发服务器

\`\`\`bash
npm run dev
\`\`\`

在浏览器中打开 [http://localhost:3000](http://localhost:3000) 查看网站。

### 构建生产版本

\`\`\`bash
npm run build
npm start
\`\`\`

## 项目结构

\`\`\`
src/
├── app/
│   ├── api/
│   │   └── chat/
│   │       └── route.ts          # AI 助手 API
│   ├── globals.css               # 全局样式
│   ├── layout.tsx                # 根布局
│   └── page.tsx                  # 主页面
├── components/
│   ├── LandingPage.tsx           # 引导页组件
│   ├── ResumePage.tsx            # 简历页组件
│   ├── EducationSection.tsx      # 教育背景
│   ├── InternshipSection.tsx     # 实习经历（可折叠）
│   ├── ProjectSection.tsx        # 项目经历
│   ├── CourseworkSection.tsx     # 课程设计（网格+模态框）
│   ├── SkillsSection.tsx         # 技能专长
│   ├── SidebarNavigation.tsx     # 侧边栏导航
│   └── ScrollReveal.tsx          # 滚动动画组件
└── data/
    └── resume.ts                 # 简历数据
\`\`\`

## 自定义配置

### 修改简历数据

编辑 `src/data/resume.ts` 文件来更新您的个人信息、教育背景、实习经历等。

### 修改颜色主题

在 `src/app/globals.css` 中修改 CSS 变量：

\`\`\`css
:root {
  --background: #0a0a0f;
  --foreground: #e4e4e7;
  --glass-bg: rgba(255, 255, 255, 0.05);
  --glass-border: rgba(255, 255, 255, 0.1);
}
\`\`\`

### 修改动画效果

在 `tailwind.config.js` 中自定义动画：

\`\`\`javascript
animation: {
  'fade-in-up': 'fadeInUp 0.6s ease-out forwards',
  'fade-in': 'fadeIn 0.8s ease-out forwards',
  'slide-in-left': 'slideInLeft 0.5s ease-out forwards',
}
\`\`\`

## AI 助手配置

要启用 AI 助手功能，需要在 `src/app/api/chat/route.ts` 中配置您的 API 密钥。

当前实现已经将完整的简历数据注入到 System Prompt 中，AI 助手可以基于这些信息回答关于具体算法、实习、课程设计等问题。

## 部署

### Vercel

1. 将代码推送到 GitHub
2. 在 [Vercel](https://vercel.com) 上导入项目
3. Vercel 会自动构建和部署

### 其他平台

项目可以部署到任何支持 Next.js 的平台，如 Netlify、Railway 等。

## 许可证

MIT License

## 联系方式

- 姓名：师鑫荣
- 邮箱：Xinrong.Shi22@student.xjtlu.edu.cn
- 电话：17622929577
