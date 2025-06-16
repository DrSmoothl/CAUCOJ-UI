# CAUCOJ DaisyUI 界面重构

这个项目是对 HydroOJ 在线判题系统的前端界面进行的全面 DaisyUI 重构。

## 🎯 重构目标

- 使用 DaisyUI 和 Tailwind CSS 替代原有的自定义 CSS 样式
- 提供现代化、响应式的用户界面
- 保持原有功能的完整性
- 提升用户体验和视觉效果

## 🛠 技术栈

- **CSS框架**: DaisyUI 4.12.10 + Tailwind CSS
- **模板引擎**: Jinja2
- **构建系统**: HydroOJ 原生构建系统

## 📝 已重构的组件

### 核心布局
- ✅ `layout/html5.html` - 基础 HTML5 布局，引入 DaisyUI
- ✅ `layout/basic.html` - 基本页面布局，使用 drawer 和现代化结构

### 导航组件
- ✅ `partials/nav.html` - 导航栏，使用 DaisyUI navbar 组件
- ✅ `partials/footer.html` - 页脚，现代化设计

### UI 组件
- ✅ `components/user.html` - 用户信息组件，使用 avatar 和 badge
- ✅ `components/form.html` - 表单组件，使用 DaisyUI 表单样式
- ✅ `components/paginator.html` - 分页器，使用 join 和 btn 组件

### 页面模板
- ✅ `main.html` - 主页，使用网格布局
- ✅ `problem_main.html` - 问题列表页，使用 card 和现代化布局
- ✅ `user_login.html` - 登录页，使用 hero 和 card 组件

## 🎨 设计特色

### 主题支持
- 支持亮色主题 (`light`)
- 支持暗色主题 (`dark`)
- 自动继承用户偏好设置

### 响应式设计
- 移动端优先设计
- 使用 Tailwind CSS 响应式网格系统
- 智能的导航栏适配

### 现代化组件
- 卡片式布局替代传统的 section
- SVG 图标替代图标字体
- 平滑的过渡动画
- 优雅的下拉菜单和提示

## 🔧 安装和使用

1. **引入 DaisyUI**
   DaisyUI 和 Tailwind CSS 已通过 CDN 引入到 `html5.html` 中：
   ```html
   <link href="https://cdn.jsdelivr.net/npm/daisyui@4.12.10/dist/full.min.css" rel="stylesheet" />
   <script src="https://cdn.tailwindcss.com"></script>
   ```

2. **主题配置**
   在 HTML 根元素上使用 `data-theme` 属性：
   ```html
   <html data-theme="light">  <!-- 或 "dark" -->
   ```

3. **自定义样式**
   自定义 CSS 变量和样式已添加到 `html5.html` 中，包括：
   - 字体设置
   - 主题颜色覆盖
   - 代码字体配置
   - 滚动条样式

## 📱 组件使用示例

### 用户信息组件
```jinja2
{{ user.render_inline(udoc, avatar=true, badge=true) }}
```

### 表单组件
```jinja2
{{ form.form_begin({label: '用户名', required: true}) }}
<input class="input input-bordered" name="username" />
{{ form.form_end() }}
```

### 分页组件
```jinja2
{{ paginator.render(page, num_pages) }}
```

## 🎯 功能特性

### 用户体验
- 直观的导航结构
- 快速的主题切换
- 清晰的视觉层次
- 一致的交互反馈

### 可访问性
- 语义化的 HTML 结构
- ARIA 标签支持
- 键盘导航友好
- 颜色对比度优化

### 性能优化
- 轻量级的 CSS 框架
- 最小化的自定义样式
- 优化的组件结构
- 快速的页面加载

## 🔄 兼容性

- ✅ 现代浏览器 (Chrome, Firefox, Safari, Edge)
- ✅ 移动端浏览器
- ✅ 保持与原有 HydroOJ 功能的完全兼容
- ✅ 向后兼容旧版模板系统

## 🚀 后续改进

- [ ] 添加更多动画效果
- [ ] 优化移动端体验
- [ ] 增加更多主题选项
- [ ] 完善组件文档
- [ ] 性能监控和优化

## 📞 技术支持

这个重构基于 DaisyUI 的最佳实践，保持了 HydroOJ 原有的所有功能，同时提供了现代化的用户界面。如果在使用过程中遇到问题，请检查 DaisyUI 官方文档或联系开发团队。

---

**注意**: 这个重构完全基于模板文件的修改，无需修改 HydroOJ 的后端代码，可以作为插件形式集成到现有系统中。
