# 🎯 Priospace

一款美观、现代的生产力应用，结合了任务管理、番茄钟计时器功能、习惯跟踪和实时协作。使用Next.js、React和Framer Motion构建，实现流畅的动画和优质的用户体验。

![Todo Timer](https://img.shields.io/badge/Version-2.1-blue)
![Next.js](https://img.shields.io/badge/Next.js-15-black)
![React](https://img.shields.io/badge/React-19-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)
![Tailwind](https://img.shields.io/badge/Tailwind-3-38bdf8)
![WebRTC](https://img.shields.io/badge/WebRTC-Enabled-green)

## ✨ 功能特性

### 📝 任务管理
- 创建、编辑和管理任务及习惯
- **子任务支持** - 将复杂任务分解为可管理的子任务
- 使用自定义颜色编码的分类组织任务
- 使用流畅动画标记任务完成
- 长按完成手势，适用于移动设备交互
- 普通任务和习惯的独立分区

### 🌐 实时协作（新增）
- **基于WebRTC的实时协作**，用于共享工作区
- 跨多个用户的实时任务更新
- 点对点连接实现即时同步
- 与团队成员实时共享任务和进度
- 初始握手后点对点连接无需服务器依赖

### ⏱️ 番茄钟计时器
- 可自定义的计时器预设（5、10、25、50分钟）
- 带动画显示的实时倒计时
- 超时跟踪，用于延长工作时段
- 带自动转换的休息计时器
- 专注时间跟踪，获取生产力洞察
- 音乐播放器风格的控件（播放/暂停/停止）

### 🔄 习惯跟踪
- GitHub风格的贡献图，显示90天的习惯历史
- 带视觉强度指示器的月度视图
- 每日完成的个人习惯跟踪
- 用于标记习惯完成的交互式网格
- 全面的习惯分析和进度可视化

### 🎨 美观的用户界面/用户体验
- 现代化的底部弹出式模态设计
- **4种精美的主题**，无缝主题选择
- 使用Framer Motion实现流畅的弹簧动画
- 针对移动和桌面设备优化的响应式设计
- 支持深色/浅色模式，增强主题系统
- 贯穿应用的主色调主题
- 直观的触摸手势和微交互

### 📊 数据管理
- 用于数据备份的导出/导入功能
- 本地存储持久化
- 带主题控制的增强设置面板
- 带随机名言的激励性介绍屏幕

## 🚀 入门指南

### 先决条件

- Node.js 18+
- npm或yarn包管理器

### 安装

1. **克隆仓库**
   ```bash
   git clone https://github.com/anoyrc/priospace.git
   cd priospace
   ```

2. **安装依赖**
   ```bash
   npm install
   # 或
   yarn install
   ```

3. **设置WebRTC服务器（用于协作功能）**
   ```bash
   cd webrtc-server
   npm install
   npm run start
   ```
   
   WebRTC信令服务器将在默认端口启动。使用协作功能前请确保此服务器正在运行。

4. **运行开发服务器**
   ```bash
   # 返回根目录
   cd ..
   npm run dev
   # 或
   yarn dev
   ```

5. **打开浏览器**
   导航到 [http://localhost:3000](http://localhost:3000)

## 🏗️ 技术栈

### 前端
- **Next.js 15** - 带有App Router的React框架
- **React 19** - 带有hooks和现代模式的UI库
- **TypeScript** - 类型安全的JavaScript开发
- **Tailwind CSS** - 实用优先的CSS框架
- **Framer Motion** - 用于流畅交互的动画库

### 实时功能
- **WebRTC** - 点对点实时通信
- **WebSocket** - 用于WebRTC握手的信令服务器
- **Node.js** - 用于WebRTC信令的后端服务器

### UI组件
- **shadcn/ui** - 高质量、可访问的UI组件
- **Lucide React** - 美观、可定制的图标
- **自定义组件** - CountdownTimer、CircleProgress和模态系统

### 状态管理
- **React Hooks** - 用于状态管理的useState、useEffect、useRef
- **Local Storage** - 浏览器中的数据持久化
- **Context API** - 主题和全局状态管理

## 📁 项目结构

```
priospace/
├── app/                    # Next.js App Router
│   ├── globals.css        # 全局样式和Tailwind导入
│   ├── layout.tsx         # 带有providers的根布局
│   └── page.tsx           # 主应用程序页面
├── components/            # 可复用组件
├── lib/                   # 工具函数
│   └── utils.ts          # 辅助函数和工具
├── webrtc-server/         # WebRTC信令服务器
│   ├── server.js         # 带WebSocket支持的Express服务器
│   ├── package.json      # 服务器依赖
│   └── ...
├── public/               # 静态资源
└── package.json          # 依赖和脚本
```

## 🎮 使用方法

### 创建带子任务的任务
1. 点击**"Add Task"**按钮
2. 在无边框输入框中输入任务标题
3. 可选择或创建带自定义颜色的分类
4. 通过点击子任务选项**添加子任务**
5. 将复杂任务分解为可管理的部分
6. 点击**"Add Task"**保存

### 实时协作
1. 启动WebRTC服务器: `cd webrtc-server && npm run start`
2. 与团队成员分享您的工作区ID
3. 实时协作处理任务和项目
4. 查看团队成员更改时的实时更新
5. 所有更改即时同步，无需刷新页面

### 使用计时器
1. 从列表中选择一个任务
2. 选择计时器预设（5、10、25或50分钟）
3. 使用音乐播放器风格的控件：
   - **播放/暂停** - 启动或暂停计时器
   - **停止** - 将计时器重置为原始时间
   - **休息** - 休息5分钟
4. 完成任务后标记完成

### 跟踪习惯
1. 从底部导航打开**习惯跟踪器**
2. 添加带分类的新习惯
3. 点击网格方块标记每日完成情况
4. 使用GitHub风格的可视化查看90天进度
5. 在习惯概览和单个习惯视图之间导航

### 主题选择
1. 访问**设置**浏览4种精美主题
2. 从增强的配色方案中选择
3. 体验无缝的主题转换
4. 主题在会话间保持

### 管理数据
1. 访问**设置**以：
   - 从4种精美主题中选择
   - 在浅色和深色模式间切换
   - 将数据导出为JSON备份
   - 导入以前导出的数据
   - 通过"Buy Me a Coffee"支持开发者

## 🔧 配置

### WebRTC服务器设置
WebRTC服务器处理点对点连接的信令：

```bash
# 默认服务器配置
cd webrtc-server
npm install
npm run start
```

对于生产部署，请在`webrtc-server/server.js`中配置服务器设置。

### 自定义主题
该应用现在支持4种主题。在设置中更新主题配置：

```css
:root {
  --primary: your-color-hue your-color-saturation your-color-lightness;
  --theme-variant: your-theme-name;
}
```

### 计时器预设
在`TimerModal.tsx`中修改计时器预设：

```javascript
const presets = [
  { value: "5", label: "5 min", seconds: 5 * 60 },
  { value: "15", label: "15 min", seconds: 15 * 60 },
  // 添加您的自定义预设
];
```

### 子任务配置
在任务组件中自定义子任务行为：

```javascript
const maxSubtasks = 10; // 限制每个任务的子任务数
const subtaskDepth = 2;  // 最大嵌套级别
```

## 🌐 WebRTC服务器说明

### 开发设置
1. **导航到WebRTC服务器目录**
   ```bash
   cd webrtc-server
   ```

2. **安装服务器依赖**
   ```bash
   npm install
   ```

3. **启动信令服务器**
   ```bash
   npm run start
   ```

服务器将处理WebRTC信令以支持实时协作功能。使用协作工作区前请确保其正在运行。

### 生产部署
对于WebRTC服务器的生产部署：

1. 配置生产环境变量
2. 设置适当的CORS策略
3. 使用PM2等进程管理器确保服务器稳定性
4. 考虑使用HTTPS以确保WebRTC连接安全

## 📱 渐进式Web应用功能

- 针对移动和桌面设备的响应式设计
- 触摸手势和针对移动设备优化的交互
- 使用本地存储持久化的离线就绪功能
- 使用Next.js优化的快速加载
- 跨设备工作的实时协作

## 🤝 贡献

1. Fork仓库
2. 创建功能分支 (`git checkout -b feature/amazing-feature`)
3. 提交更改 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 打开拉取请求

### 开发指南
- 遵循现有的代码风格和组件模式
- 使用TypeScript确保类型安全
- 使用Framer Motion添加适当动画
- 确保响应式设计在所有屏幕尺寸上正常工作
- 测试所有4种主题的一致性
- 测试多个对等点的WebRTC功能
- 维护无障碍标准
- 彻底测试子任务功能

## 🐛 错误报告和功能请求

请使用[GitHub Issues](https://github.com/anoyrc/priospace/issues)页面：
- 报告带有详细重现步骤的错误
- 请求带有明确用例的新功能
- 讨论改进和建议
- 报告WebRTC连接问题

## 📄 许可证

该项目基于MIT许可证 - 详情请见[LICENSE](LICENSE)文件。

## 🙏 致谢

- **shadcn/ui** 提供了精美的组件库
- **Framer Motion** 提供了流畅的动画
- **Lucide** 提供了图标集
- **Tailwind CSS** 提供了实用优先的样式方法
- **Next.js** 团队提供了出色的React框架
- **WebRTC** 社区提供了实时通信标准

## 💖 支持

如果您觉得这个项目有帮助，请考虑：

- ⭐ 给仓库加星
- 🐛 报告错误或请求功能
- ☕ [给我买杯咖啡](https://coff.ee/anoy)
- 🐦 在Twitter上关注[@Anoyroyc](https://x.com/Anoyroyc)

---

<div align="center">

### 🎯 vibecoded

**由[Anoy Roy Chowdhury](https://x.com/Anoyroyc)用心编码**

*专注 • 跟踪 • 实现 • 协作*

</div>