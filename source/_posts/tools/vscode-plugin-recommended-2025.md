---
title: 2025 前端开发 vscode 常用插件推荐
link: vscode-plugin-recommended-2025
catalog: true
lang: cn
date: 2025-03-29 18:03:44
tags:
  - 前端
  - vscode
categories:
  - 工具
---

总结了下自己的 2024 至今的常用前端插件以及工具推荐，上次写还是在上一次：[2022 前端开发 vscode 常用插件及其他工具推荐](https://ysx.cosine.ren/vscode-plugin-recommended-2022/)

本次写推荐我会把相比之前新增的特意标出来一下放前面，不代表后面的就不好用，有些插件越用越爽～并且清理了一波使用不多的插件。这么看下来其实我插件也没有很多吧，虽然常用编辑器换到 cursor 了但是插件还没有开始进行发掘。

## 开发类

### [New] Shader languages support for VS Code

评语：webGL 开发必备

[Shader languages support for VS Code](https://marketplace.visualstudio.com/items?itemName=slevesque.shader) 是一款为 VS Code 提供着色器语言支持的强大插件，专为图形编程和游戏开发者设计，该插件支持以下三种主要的着色器语言：

- HLSL - 高级着色语言（High-Level Shading Language），主要用于 DirectX
- GLSL - OpenGL 着色语言（OpenGL Shading Language）
- Cg - C for Graphics，NVIDIA 的着色器语言

![Example](https://r2.cosine.ren/i/2025/03/29/156ajl-cm.webp)

### [New] Tailwind CSS ClassName Highlight

评语：超级棒，[hyoban](https://github.com/hyoban) 开发，有效类名一眼就能看出来。

[Tailwind CSS ClassName Highlight](https://marketplace.visualstudio.com/items?itemName=hyoban.tailwindcss-classname-highlight)

灵感来自于 UnoCSS 的 VS Code 扩展，让开发者能够直观地分辨哪些 Tailwind 类名是有效的。

- 限制：该插件无法检测不生成任何 CSS 的有效类名，例如 group 和 prose 等功能类。

Github 仓库：<https://github.com/hyoban/tailwindcss-classname-highlight>

![Example](https://r2.cosine.ren/i/2025/03/29/14a26h-52.gif)

### [New] shadcn Color Preview

评语：结合 shadcn 食用查看颜色、十六进制转 hsl 很方便

[shadcn Color Preview](https://marketplace.visualstudio.com/items?itemName=dexxiez.shadcn-color-preview) 是一款专为 Visual Studio Code 开发的颜色预览插件。它主要功能是为使用 shadcn 语法的 HSL 颜色值提供实时预览，极大地提高了开发效率。

- 简单实用：正如其名，它能够在 CSS 文件中为使用 shadcn CSS 变量语法定义的 HSL 颜色提供直观的预览
- 颜色转换工具：提供实用的颜色转换功能，方便开发者快速转换不同颜色格式

![Example](https://r2.cosine.ren/i/2025/03/29/14f5wm-vr.webp)

### [New] react i18n

评语：i18n 用，谁用谁知道。

[react i18n](https://marketplace.visualstudio.com/items?itemName=think2011.react-i18n) 是一款非常实用的 VSCode 插件，专为使用 i18next 的 React 项目设计。正如插件的开发者所说："因为写 i18n 真的很啰嗦很麻烦啊 😫"，这个插件能够帮助你更方便地查看和编写国际化文案。主要功能

- 提取并自动翻译文案（快捷键 ⌘+.）
- 直观查看对应的翻译文案
- 通过翻译中心管理翻译
- 支持 Google、Youdao、Baidu 在线翻译
- 字段自动补全
- 自动/手动配置翻译目录
- 可指定翻译源语言
- 重复、覆盖检测
- YAML 支持

![Example](https://r2.cosine.ren/i/2025/03/29/14ugxp-xa.webp)

### [New] Rainbow CSV

评语：有过 CSV 文件的需求的时候用过，真的很棒。

[Rainbow CSV](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv) 是一款强大的 CSV 文件处理插件，它能够使 CSV、TSV 和其他分隔符文件更加易读易用。

- 使用不同颜色高亮显示 CSV、TSV、分号分隔和管道分隔文件中的列
- 通过内置的类 SQL 查询语言（RBQL）进行数据查询、转换和过滤
- 最多可以跟踪 3 个感兴趣的列，提供辅助装饰
- 以图形方式或额外空格对齐列，并可以收缩（去除字段中的空格）
- 可选的固定标题行
- 悬停时提供列信息
- 自动 CSV 一致性检查（CSVLint）
- 可选的交替行背景颜色，提高可读性
- 多光标列编辑
- 可在浏览器中使用（vscode.dev）
  该插件支持多种分隔符，包括逗号、制表符、分号、空格和管道符等。它会自动检测"纯文本"和".csv"文件的分隔符，也支持自定义任意字符或字符串作为分隔符。
  对于处理大型 CSV 文件的开发者来说，Rainbow CSV 提供了虚拟对齐和空格对齐两种模式，让表格更易阅读。同时，它的列跟踪功能和交替行背景高亮功能对于多列表格尤其有用。
  Rainbow CSV 还包含一个强大的 RBQL 查询语言解释器，允许你使用类似 SQL 的查询来操作 CSV 数据，例如：

![Example](https://r2.cosine.ren/i/2025/03/29/14ze3f-h7.webp)

### GitLens — Git supercharged

[eamodio.gitlens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

GitLens 是前端开发必备的 Git 插件之一，它不仅提供了丰富的可视化功能，还能帮助你更好地理解代码的演变历史和作者信息。这对于团队协作和代码审查尤为重要。

他提供了丰富的 git 可视化功能，现在仍然强推，我一直觉得用 GUI 不妨碍学 CLI，好的 GUI 也是很重要的。其中我最喜欢的是 File History 和 Line History，能够很清晰的知道这个文件甚至到这一行曾经有哪些 git 提交修改，帮了我很多大忙。不过 GitLens 改版之后聚在一块了，我个人比较喜欢 Detach All Views 用旧版的排布，并且 File History 和 LineHistory 原本是在另一个 tab 我一般会拖到 git 的 tab，如图：

![23478f58-0039-4081-a243-442ea71b9bb6.webp](https://r2.cosine.ren/i/2025/03/29/12opr9-b4.webp)

### Auto Close Tag

自动闭合 HTML、JSX 标签

![Example](https://backblaze.cosine.ren/juejin/Dc6e378b853b44cd9d8a17792c91c04a~Tplv-K3u1fbpfcp-Zoom-1.png)

### Auto Rename Tag

自动 rename 标签

![Example](https://backblaze.cosine.ren/juejin/Ca513e2974614bbcb89c73cf87aaa14a~Tplv-K3u1fbpfcp-Zoom-1.png)

### change-case

命名转换 Ctrl+Shift+P 输入 change case

![Example](https://backblaze.cosine.ren/juejin/588d36d067294b53bbf0c6b2f174a2d2~Tplv-K3u1fbpfcp-Zoom-1.png)

![Example](https://backblaze.cosine.ren/juejin/03367e095e0e440caaff6e4af787ffdb~Tplv-K3u1fbpfcp-Zoom-1.png)

### Code Spell Checker

代码中的拼写检查

![Example](https://backblaze.cosine.ren/juejin/A03c0981961d42ef9e8e311931bfc748~Tplv-K3u1fbpfcp-Zoom-1.png)

![Example](https://backblaze.cosine.ren/juejin/08c094fba8f84c349e08726d58e75e7a~Tplv-K3u1fbpfcp-Zoom-1.png)

### ES7 React/Redux/GraphQL/React-Native snippets

React 代码片段，如图，比较常用的就是输入 rfc 等补全，当然现在 AI 时代了 cursor 也会补全，使用频率大幅下降。

![Example](https://backblaze.cosine.ren/juejin/90c733f72f704973b55355beaf1bf189~Tplv-K3u1fbpfcp-Zoom-1.png)

### Commit Message Editor

git 提交信息的编辑，其实现在不怎么常用了，主要是已经记得滚瓜烂熟了，但是还留着。

![Example](https://backblaze.cosine.ren/juejin/0819b66cd6764219a37e795c454397d0~Tplv-K3u1fbpfcp-Zoom-1.png)

### ESLint

![Example](https://backblaze.cosine.ren/juejin/E821b84d00164ef28e24db4a457f2478~Tplv-K3u1fbpfcp-Zoom-1.png)

### Prettier

这个要注意一下版本的坑...说来话长了

指定配置文件.prettierrc.js，方便在项目中通过自己项目的 prettier 配置文件进行格式化

Why Prettier？ <https://prettier.io/docs/en/why-prettier.html>

![Example](https://backblaze.cosine.ren/juejin/790d631cc229421dafbd8c63b9e5bbc9~Tplv-K3u1fbpfcp-Zoom-1.png)
![Example](https://backblaze.cosine.ren/juejin/D1e5582cd0914923baddb6a3f9e1198b~Tplv-K3u1fbpfcp-Zoom-1.png)

![Example](https://backblaze.cosine.ren/juejin/8884949755674c40a77d6ad2b6140e6b~Tplv-K3u1fbpfcp-Zoom-1.png)

### Tailwind CSS IntelliSense（使用 Tailwind 推荐）

tailwind 的自动补全，智能提示

![Example](https://backblaze.cosine.ren/juejin/5efb09a2a26646588bfce90b4c9b4dd4~Tplv-K3u1fbpfcp-Zoom-1.png)

### Error Lens

改进对错误、警告和其他语言诊断的突出显示。

![Example](https://backblaze.cosine.ren/juejin/325ca1837fff44dd98d1d00acdcb98f5~Tplv-K3u1fbpfcp-Zoom-1.png)

### px to rem & rpx & vw (cssrem)

顾名思义，响应式开发的好帮手，方便的进行单位转换，可以 Alt + Z 将 px 值转换为 rem

![Example](https://backblaze.cosine.ren/juejin/F4b75e2133cf4f1081fffc12222dae26~Tplv-K3u1fbpfcp-Zoom-1.png)

### Template String Converter

在字符串中输入 `${` 后自动将其变为模板字符串

![Example](https://backblaze.cosine.ren/juejin/89f5f71adbdb4f2197b12b804ff348dd~Tplv-K3u1fbpfcp-Zoom-1.png)

### TabOut

也是用习惯了就回不去的插件，按 Tab 跳出括号

![Example](https://backblaze.cosine.ren/juejin/Ea8b7baf5183478d991298fb91e97a83~Tplv-K3u1fbpfcp-Zoom-1.png)

### vscode-styled-components（使用 styled-components 推荐）

![Example](https://backblaze.cosine.ren/juejin/6b25d9386b594ae8b4e59cc2bff209a8~Tplv-K3u1fbpfcp-Zoom-1.png)

### Highlight Matching Tag

顾名思义，高亮标签插件

![Example](https://backblaze.cosine.ren/juejin/48d1d3b2d475461d99786b592a2aea6e~Tplv-K3u1fbpfcp-Zoom-1.png)

### Live Server

[Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) 为静态和动态页面启动一个具有实时重载功能的本地开发服务器，比较经典的插件了，适合实时预览 HTML 单文件的场景，比如一些小 demo

<https://juejin.cn/post/7006338919767736357>

![Example](https://backblaze.cosine.ren/juejin/313f863f15a74da1b05d330c3648269a~Tplv-K3u1fbpfcp-Zoom-1.png)

同类插件还有个 [Live Server Preview](https://marketplace.visualstudio.com/items?itemName=negokaz.live-server-preview) 在 vscode 中就能打开一个，不用切出去

### Parameter Hints

函数参数智能提示，不过用多了就会觉得有点干扰。

![Example](https://backblaze.cosine.ren/juejin/3f6e7a6b6c884acc9863ad05ec4644fd~Tplv-K3u1fbpfcp-Zoom-1.png)

## 辅助类

### [New] SVG Gallery

评语：非常好用，批量查看 SVG 的的王者，点进去可以再 open 原始文件。
[SVG Gallery](https://marketplace.visualstudio.com/items?itemName=developer2006.svg-gallery) 非常好用。它专为开发者提供了便捷的 SVG 图像查看体验。这款插件允许您以画廊形式浏览项目中的所有 SVG 文件，极大地提高了前端开发中对矢量图资源的管理效率。主要功能包括：

- 以画廊模式查看目录下所有 SVG 图像
- 支持打开并预览单个 SVG 文件（并编辑）
- 显示图像的宽度和高度信息
- 提供刷新按钮，实时更新图像列表
- 在资源管理器右键菜单中添加"在 SVG Gallery 中打开"选项
- 支持浅色和深色主题，适应不同工作环境

![Example](https://r2.cosine.ren/i/2025/03/29/16311n-na.webp)

### [New] Tailwind Documentation

评语：cmd + ctrl + t 快捷打开 tailwind 文档现查，熟练度上升导致现在使用很少但是还是推一下。

[Tailwind Documentation](https://marketplace.visualstudio.com/items?itemName=alfredbirk.tailwind-documentation)

![Example](https://r2.cosine.ren/i/2025/03/29/141vqa-rp.webp)

### [New] Figma for VS Code

评语：这个是真有用，还原设计稿不用切俩窗口了 2333 有时候看字号等很快速。

[Figma for VS Code](https://marketplace.visualstudio.com/items?itemName=figma.figma-vscode-extension) 是一款强大的扩展插件，它将 Figma 设计工具直接带入您的代码编辑器中，极大地提升了设计师与开发者之间的协作效率。通过消除上下文切换和繁琐的工作流程，开发者可以更高效地将设计转化为代码。

### Image Gallery

批量看图片资源贼好用，推荐一手

![Example](https://backblaze.cosine.ren/juejin/F1722f02482147eda921db1614fec4e7~Tplv-K3u1fbpfcp-Zoom-1.png)
![Example](https://r2.cosine.ren/i/2025/03/29/15xkt5-as.webp)

### Image preview

图片链接预览 不必多说的好用。

![Example](https://backblaze.cosine.ren/juejin/6e9db535485a4bb1bbf6fe7e8770393b~Tplv-K3u1fbpfcp-Zoom-1.png)

### Project Manager

vscode 的项目管理器，一键切换项目，现在依然是我很喜欢的插件，还可以打标签。

![Example](https://backblaze.cosine.ren/juejin/Bcf067868c9143fda8491a84501ccc81~Tplv-K3u1fbpfcp-Zoom-1.png)

![Example](https://backblaze.cosine.ren/juejin/695e0dd44e4f43ae88759a94405e0049~Tplv-K3u1fbpfcp-Zoom-1.png)

### Todo Tree

顾名思义 展示项目中注释的 TODO 在哪，只需要 TODO 自动就会高亮。

![Example](https://backblaze.cosine.ren/juejin/3fe9ed9022de45cd97078a69f779ea19~Tplv-K3u1fbpfcp-Zoom-1.png)
![Example](https://backblaze.cosine.ren/juejin/62cdfa90c330480886ffd2595cc82f25~Tplv-K3u1fbpfcp-Zoom-1.png)

### Comment Translate

注释翻译，如图，太有用了哥们。

![Example](https://backblaze.cosine.ren/juejin/7ebfb335a8384ef79d9b34a828c965e4~Tplv-K3u1fbpfcp-Zoom-1.png)

### Code Runner

这个想必不用多说，右上小三角运行代码

![Example](https://backblaze.cosine.ren/juejin/936e0d6de2d444afae35b5ce6740f11c~Tplv-K3u1fbpfcp-Zoom-1.png)

## 实用工具类

### [New] SQLite3 Editor

评语：一款非常强大的 SQLite 数据库编辑工具，可以像操作电子表格一样编辑本地 SQLite 数据库文件，喜欢 SQLite 的应该喜欢用。

[SQLite3 Editor](https://marketplace.visualstudio.com/items?itemName=yy0931.vscode-sqlite3-editor) 是一个允许您无需编写 SQL 查询就能编辑 SQLite 3 文件的强大插件。它提供了类似电子表格应用程序的界面体验，使数据库操作变得直观简单。

![image.webp](https://r2.cosine.ren/i/2025/03/29/15e39q-h9.webp)

### [New] project-tree

评语：挺实用的，Ctrl + Shift + P 然后输入 Project Tree 就能生成类似这样的树形目录。

[project-tree](https://marketplace.visualstudio.com/items?itemName=zhucy.project-tree) 主要功能是在项目的 README.md 文件中自动生成整个项目的树形目录结构，非常适合用于项目文档的维护和展示。

```text
project-tree
├─ .git
├─ .gitignore
├─ package-lock.json
├─ package.json
├─ src
│  ├─ config.ts
│  ├─ extension.ts
│  ├─ ignore
│  │  └─ index.ts
│  ├─ ignore.ts
│  ├─ index.ts
│  ├─ test
│  │  ├─ extension.test.ts
│  │  └─ index.ts
│  ├─ theme
│  │  ├─ index.ts
│  │  ├─ normal.ts
│  │  └─ perfect.ts
│  ├─ traverse.ts
│  ├─ type
│  │  └─ index.ts
│  └─ utils.ts
├─ tsconfig.json
├─ tslint.json
└─ webpack.config.js
```

### Bookmarks

vscode 的书签

![Example](https://backblaze.cosine.ren/juejin/696877e1c8a9473c97921ef9cb815b3d~Tplv-K3u1fbpfcp-Zoom-1.png)

### :emojisense:

方便的输入 emoj 表情

![Example](https://backblaze.cosine.ren/juejin/D73565c91ec443be8da4dc03ecaf5b50~Tplv-K3u1fbpfcp-Zoom-1.png)

### CodeTour

阅读源码时适用

![Example](https://backblaze.cosine.ren/juejin/Eaca76b552934134b41b20077efc39fa~Tplv-K3u1fbpfcp-Zoom-1.png)

### vscode-pdf

vscode 中看 pdf 文件

![Example](https://backblaze.cosine.ren/juejin/58cbee89c4bf49538e082a6cc357b734~Tplv-K3u1fbpfcp-Zoom-1.png)

### Office Viewer(Markdown Editor)

pdf 都能看了看 office 文件当然也有插件，这个跟 typora 插件一样集成 [Vditor](https://b3log.org/vditor/) 可以写 md 文件

![Example](https://backblaze.cosine.ren/juejin/A6aa7cbdb3e94f009d750645ada69fe0~Tplv-K3u1fbpfcp-Zoom-1.png)

### CodeSnap

选中代码并生成漂亮的截图

![Example](https://backblaze.cosine.ren/juejin/3a67b45e390c49d783c3c76c5ca51c75~Tplv-K3u1fbpfcp-Zoom-1.png)

### Draw.io Integration

后缀名为.drawio 的文件可以绘制流程图等，适合写技术文档，无需多言

![Example](https://backblaze.cosine.ren/juejin/4acafe3cb6e24f2b959227f6afaa7609~Tplv-K3u1fbpfcp-Zoom-1.png)

## 外观改善类

### [New] Power Mode

评语：太花里胡哨了但是有人就好这一口（比如我，悲）代码仪式感，连击的快乐，只开一点点功能就够了。

[Power Mode](https://marketplace.visualstudio.com/items?itemName=hoovercj.vscode-power-mode) 当你打字时，会在光标处显示各种视觉效果，如爆炸、粒子、传送门等...

这款插件最初在 Code in the Dark 活动中流行，现在已经被移植到 VS Code 中，主要特点：

- 强力爆炸效果：当你打字时，会在光标处显示爆炸、粒子等视觉效果
- 屏幕震动：敲击键盘时屏幕会轻微震动，带来更加强烈的打字反馈
- 组合计数器：显示连续打字的组合数，类似游戏中的连击计数
- 多种视觉效果：提供了丰富的内置效果选择，包括粒子、传送门、烟花、火焰、魔法等

![Example](https://raw.githubusercontent.com/hoovercj/vscode-power-mode/7bbc4f68dd46da883b24011ae67516c861d09d1b/images/demo-v3.gif)

### vscode-icons

[vscode-icons](https://marketplace.cursorapi.com/items?itemName=vscode-icons-team.vscode-icons)

改进 vscode 的文件图标，必备。

![Example](https://backblaze.cosine.ren/juejin/61c4203228ce4f6bb4e5d835ee456269~Tplv-K3u1fbpfcp-Zoom-1.png)

![Example](https://backblaze.cosine.ren/juejin/4756cb5e4911429cbeb93e83cac5afa9~Tplv-K3u1fbpfcp-Zoom-1.png)
![Example](https://backblaze.cosine.ren/juejin/8dbd8cd16e3045459a60f6e7e0d33fdc~Tplv-K3u1fbpfcp-Zoom-1.png)

## 其他工具

- 如果在 win 开发，那么 [AltSnap] 是一款免费开源的 Windows 小工具软件，按住 Alt 可以移动窗口和调整窗口大小透明度等，对设计稿也特别好用。
- ...先到这吧我太饿了去吃个饭先。

## 已弃用 / 禁用

这里的弃用可能是由于各种原因，不代表他就不好用，如其实没啥用到的场景、实际开发中会导致卡顿啊内存泄露啊等。

- Live Share 多人协同，共同编辑，共享终端
  - 这个工作以后真没啥用到的场景（
- Dev Containers （docker 开发适用）打开 docker 容器内的文件，用 docker 开发的都说好。
  - 这个也是用到的场景不多 hhh
- CSS Modules （CSS module 模式必备）
  - 不好意思啊近几年开发不用 CSS Module 了（呜呜呜
- 自动补全、文档类：GitHub Copilot、Tabnine AI, Codeium, Mintlify Doc Writer 等
  - 由于主力编辑器变成 cursor 了实际上全都用不上了。
- 刷题类也都弃用了
