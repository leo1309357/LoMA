# LoMA — 复古拟物视觉设计语言

> **有温度的界面，可感知的材质，可理解的秩序。**  
> Warm surfaces · Tactile controls · Editorial clarity

| 文档属性 | 内容 |
| --- | --- |
| 名称 | LoMA |
| 文档类型 | 视觉设计语言 / UI 主题规范 |
| 版本 | 1.0.0（初稿） |
| 日期 | 2026-11-26 |
| 风格定位 | 克制拟物主义 · 早期 Web 2.0 · 复古杂志排版 |
| 适用范围 | 网站、内容平台、桌面应用、工具型 WebUI、游戏菜单与资料界面 |
| 参考蓝本 | `deepseek_html_20261126_c60833.html`（Pixel Journal / 像素志） |

本文件定义 LoMA 的视觉语法，而非限定一套固定的网站模板。所有采用 LoMA 的产品应在色彩、材质、光照、边界、排版与交互反馈上保持一致；内容、布局与品牌信息可以依据具体产品变化。

**规范用语：**「必须」表示保持风格或可用性的必要规则；「应」表示推荐默认值；「可」表示在不违背核心原则的前提下允许调整的项目。

---

## 1. 设计哲学

LoMA 以 2010 年前后网页中常见的渐变、内高光、细边框、纸质纹理和编辑式排版为出发点，在现代界面中恢复适度的实体感。它不追求对现实物体的逐像素模仿，也不将所有界面元素做成立体物件，而是以材质暗示建立空间关系，以真实而克制的反馈建立操作直觉。

### 1.1 核心原则

| 原则 | 设计要求 |
| --- | --- |
| **Material Honesty · 材质诚实** | 背景像纸，承载层像卡纸，导航框架像深色涂装金属，控制件像可以触碰的实体。材质随功能而变化。 |
| **Tactile Affordance · 触感直觉** | 可以按压的部件具有凸起、高光与底缘暗部；激活时出现真实的压入感。不可操作的内容层不伪装成按钮。 |
| **Editorial Order · 编辑秩序** | 使用衬线标题、清晰栏位、细分隔线、紧凑但呼吸自然的信息结构，接近一本排版良好的杂志。 |
| **Restrained Ornament · 克制装饰** | 装饰必须服务于层级。纹理低对比，阴影短而柔和，不让光效压过内容。 |
| **Modern Usability · 现代可用性** | 复古表达不等于复古的交互限制。必须保留键盘导航、可访问状态、移动端操作与清晰的阅读对比度。 |

### 1.2 风格边界

LoMA 是**轻度至中度拟物化**视觉语言：

- 不是纯扁平设计：不可将关键操作件的形态全部退化为无边界纯色矩形。
- 不是极端拟物：不使用大面积皮革、木纹、铆钉、仪表盘或重度照片纹理作为默认装饰。
- 不是玻璃拟态：不以背景模糊、透明玻璃和霓虹轮廓作为主要层级机制。
- 不是新拟态：不依赖同背景色双向阴影构建所有控件，必须保留清晰的可辨识边界。
- 不是怀旧滤镜：不靠扫描线、失真、做旧污渍或低分辨率来制造年代感。

## 2. 蓝本特征提炼

以下值直接取自参考 HTML 的 CSS；后文将其抽象为通用设计规则，并在必要之处作现代化延伸。

| 原始特征 | 蓝本参数 | LoMA 语法 |
| --- | --- | --- |
| 纸张底色 | `#E8E4DC`，双层径向柔光及 45° 细纹 | 暖中性色画布，纹理轻于内容 |
| 深色导航 | `#4A5A6A → #35424F → #2B3642` | 冷色结构部件、顶部亮边、下缘阴影 |
| 卡片 | `#FDFCF9`，1px 暖灰边框，6px 圆角 | 纸质承载面，微弱抬升 |
| 主按钮 | `#E8B04B → #D4942A → #C07F1A` | 琥珀色模压实体、内高光、按下凹陷 |
| 链接 | `#C0392B` | 砖红色强调，用于可点击文字 |
| 字体 | Georgia 标题；Helvetica / Arial 正文 | 衬线表现编辑与品牌，非衬线保证操作阅读 |
| 内容宽度 | 960px；双栏间隔 24px；侧栏 280px | 居中规则网格，主次叙事结构 |
| 列表 | 14px 纵向间距，虚线分隔 | 水平节奏清晰的索引式信息组织 |
| 圆角 | 按钮 5px，卡片 6px，标签 12px | 普通实体小圆角；胶囊仅用于标签等特殊部件 |
| 过渡 | 150–200ms | 短促、局部、与状态关联的过渡 |

**保留的视觉签名：**暖纸底色 + 冷蓝灰框架 + 琥珀操作件 + 细描边 + 单向光照 + 衬线标题。即使在没有主图的界面中，这些特征仍应使 LoMA 可被辨识。

## 3. 色彩系统（Color）

### 3.1 基础色板

默认主题为暖色浅色主题；以下为 sRGB 十六进制值。品牌色是材质体系的一部分，不要求每个组件使用琥珀色。

| 令牌 | 颜色 | 用途 |
| --- | --- | --- |
| `canvas` | `#E8E4DC` | 全局暖纸背景 |
| `canvas-deep` | `#DDD8CE` | 页脚、背景下缘、次级区域 |
| `surface` | `#FDFCF9` | 卡片、正文、弹窗内容面 |
| `surface-muted` | `#F0ECE3` | 标签底面、次级面板 |
| `border` | `#D6D0C4` | 暖灰结构边界 |
| `divider` | `#E3DDD1` | 内容细分隔线 |
| `divider-dashed` | `#DDD6C8` | 列表虚线 |
| `slate-light` | `#4A5A6A` | 深色框架高光 |
| `slate-mid` | `#35424F` | 深色框架主体 |
| `slate-dark` | `#2B3642` | 深色框架暗部、标题文字 |
| `slate-border` | `#1E262E` | 深色框架边缘 |
| `amber-light` | `#E8B04B` | 主操作件及品牌高光 |
| `amber-mid` | `#D4942A` | 主操作件主体 |
| `amber-dark` | `#C07F1A` | 主操作件暗部 |
| `amber-border` | `#A86A10` | 主操作件边缘 |
| `brick` | `#C0392B` | 链接、强调 |
| `brick-strong` | `#A2382C` | 暖纸背景上的高对比链接 |
| `text` | `#3A3A3A` | 默认正文 |
| `text-body` | `#4A4A4A` | 卡片正文 |
| `text-muted` | `#736B60` | 白卡上的元信息 |
| `text-on-canvas-muted` | `#625A4E` | 暖纸底色及页脚上的小字 |
| `text-amber` | `#2C1B08` | 琥珀按钮深色标签 |
| `text-inverse` | `#F5F2EA` | 深色框架文字 |
| `text-nav` | `#D8DDE3` | 导航项文字 |
| `tag-text` | `#5A6A7A` | 浅色标签文字 |
| `focus` | `#28628A` | 键盘焦点环 |

### 3.2 色彩使用规则

- 结构以暖中性色为主；深蓝灰用于导航、窗口标题栏、工具栏及关键标题。
- 琥珀是**操作强调色**，应首先分配给主操作、选中的关键选项或小面积品牌标记。
- 砖红是**文本强调色**，可用于链接，但错误状态必须同时具备文字或图标，不仅靠颜色。
- 推荐视觉面积比例：暖中性色 70–85%，深蓝灰框架 10–20%，强调色 3–10%。这是界面整体的参考区间，不要求机械匹配。
- 禁止在每个卡片上加入高饱和渐变、彩色边框或无意义色带。
- 原 HTML 的 `#9A9286` 浅色元信息和琥珀按钮上的白字是复古表现的一部分；LoMA 默认不沿用这两个低对比搭配。使用上述高对比令牌替代。

### 3.3 功能色（扩展）

| 状态 | 前景色 | 浅底色 | 表达 |
| --- | --- | --- | --- |
| 成功 | `#35664E` | `#E8F0E6` | 勾选图标 + 状态文字 |
| 提示 | `#345E80` | `#E7EDF3` | 信息图标 + 说明 |
| 警告 | `#79500D` | `#F5EAD2` | 警示图标 + 处理建议 |
| 错误 | `#A2382C` | `#F6E5DF` | 错误图标 + 具体原因 |

功能色应优先用于小范围标记和通知，不替代整个系统的材质基调。

## 4. 材质、光照与空间

### 4.1 材质角色

| 材质 | 界面角色 | 表现方式 |
| --- | --- | --- |
| Paper · 暖纸 | 页面画布 | 微弱纸纹、细腻漫反射，不设置厚边 |
| Cardstock · 卡纸 | 内容卡片、资料区域 | 接近白色、细暖灰描边、短柔影 |
| Coated Metal · 涂装金属 | 导航、控制框架 | 深蓝灰纵向渐变、顶部 1px 高光、底缘暗线 |
| Molded Enamel · 模压搪瓷/软质塑料 | 按钮、控制件 | 色彩渐变、内高光、边界与按压状态 |
| Recess · 凹槽 | 输入框、搜索框、进度槽 | 浅色内阴影、稳定外边界 |
| Image Print · 印刷图像 | 封面、头条、媒体内容 | 图像本身保留色调，边缘裁切、必要的标题遮罩 |

每个组件只应使用一种主材质，最多叠加一层服务于信息的覆盖效果。材质指视觉隐喻，不要求引入真实物理渲染。

### 4.2 光照模型

- 默认光源位于**正上方略偏左**，所有实体的明暗关系应统一。
- 凸起部件：上亮、下暗；顶部 1px 内高光；外阴影主要向下。
- 凹陷部件：上缘内暗、内部浅亮；禁止同时使用明显凸起外影。
- 卡片只做微弱抬升，不应像按钮一样具有强烈的表面渐变。
- 文字阴影只用于深色导航、品牌标题或影像覆盖文字，推荐 `0 1px 1px rgba(0,0,0,.45)`；正文不使用文字阴影。
- 禁止通过多方向彩色光源、重度白色高光或大面积镜面反射制造不一致的层次。

### 4.3 渐变

| 用途 | 规范 |
| --- | --- |
| 深色框架 | 自上而下，`#4A5A6A 0%, #35424F 50%, #2B3642 100%` |
| 琥珀按钮 | 自上而下，`#E8B04B 0%, #D4942A 50%, #C07F1A 100%` |
| 次级控制件 | 自上而下，`#FDFCF9 0%, #F0ECE3 55%, #E1DBD0 100%` |
| 页脚 | 自上而下，`#E8E4DC → #DDD8CE` |
| 图像遮罩 | 自下而上由深色半透明过渡至透明；实际文字区域必须保证对比度 |

控制件使用 2–3 个色标即可形成体积，不应加入突兀的分界线或过强的光泽。渐变方向可用于表示压入状态，但不应当仅为了装饰而变化。

### 4.4 纸张微纹理

参考网页中的纹理可直接用 CSS 复现；底色仍以纯色作为回退：

```css
.loma-canvas {
  background-color: var(--loma-canvas);
  background-image:
    radial-gradient(circle at 20% 30%, rgb(255 255 255 / 60%) 0%, transparent 40%),
    radial-gradient(circle at 80% 70%, rgb(255 255 255 / 40%) 0%, transparent 35%),
    repeating-linear-gradient(
      45deg, rgb(0 0 0 / 1.2%) 0 1px, transparent 1px 6px
    );
}
```

纹理不应干扰中英文笔画、小字、表单和图标；不要把斜纹重复叠加到每张卡片或按钮。大面积局部纹理的透明度应保持低水平，必要时提供无纹理模式。

### 4.5 阴影等级

| 等级 | CSS 阴影 | 用途 |
| --- | --- | --- |
| E0 · 基面 | `none` | 纸面、文字、普通分隔区域 |
| E1 · 卡纸 | `0 1px 3px rgb(0 0 0 / 8%), 0 4px 12px rgb(0 0 0 / 5%)` | 卡片、静态面板 |
| E2 · 控制件 | `inset 0 1px 0 rgb(255 255 255 / 40%), 0 1px 2px rgb(0 0 0 / 20%)` | 按钮、浮起的控制件 |
| E3 · 框架 | `inset 0 1px 0 rgb(255 255 255 / 15%), 0 2px 4px rgb(0 0 0 / 20%)` | 顶栏、固定工具栏 |
| E4 · 浮层 | `0 1px 2px rgb(0 0 0 / 15%), 0 6px 18px rgb(0 0 0 / 12%)` | 封面、菜单、弹出面板 |
| I1 · 凹陷 | `inset 0 1px 3px rgb(0 0 0 / 12%)` | 输入及凹槽 |
| I2 · 按下 | `inset 0 2px 4px rgb(0 0 0 / 25%)` | 处于按压中的按钮 |

阴影等级对应功能与位置，不表示所有较高编号都必须比前一级更深。弹窗可在 E4 基础上加深扩散范围，但同一视图不宜堆叠多个强阴影层。

## 5. 几何系统

- **基本描边：**1 CSS px。内容边框可低对比；表单、焦点及交互边界应清晰可辨。
- **普通圆角：**4–6px。大面积内容面不应采用过大的现代卡片圆角。
- **小控件圆角：**4px；按钮 5px；标准卡片、封面和对话框 6px。
- **标签圆角：**12px 或等于控件高度的一半；胶囊不是通用按钮的默认形态。
- **圆形控件：**仅用于头像、图标按钮、状态指示等有明确功能的对象。
- **焦点环：**2px 实线、外偏移 2px；深色表面用浅色环，同时保持足够对比度。
- 不允许边缘过度倒角、同一组件内多重装饰描边或无功能的倾斜形体。

## 6. 排版（Typography）

### 6.1 字体

```css
--loma-font-ui: "Helvetica Neue", Helvetica, Arial, "PingFang SC",
  "Microsoft YaHei", "Noto Sans CJK SC", sans-serif;
--loma-font-heading: Georgia, "Times New Roman", "Songti SC",
  "Noto Serif CJK SC", SimSun, serif;
--loma-font-mono: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
```

衬线用于品牌字标、文章标题、章节标题；非衬线用于正文、导航和操作控件。中文标题应有合适的宋体类后备字体，防止拉丁 Georgia 与中文默认黑体形成意外风格差异。工具数据、代码与编号可使用等宽字体，不扩大到普通正文。

### 6.2 字阶

| 层级 | 字号 | 行高 | 字重 / 字体 |
| --- | --- | --- | --- |
| H1 / 封面标题 | 30px | 1.25 | 700，衬线 |
| 页面标题 / 品牌 | 22–26px | 1.3 | 700，衬线 |
| H2 / 卡片标题 | 20px | 1.35 | 700，衬线 |
| H3 / 小部件标题 | 16px | 1.4 | 700，衬线 |
| 列表条目标题 | 16px | 1.45 | 600–700，衬线 |
| 正文 | 14px | 1.6 | 400，非衬线 |
| 长文阅读（扩展） | 15–16px | 1.7–1.85 | 400，非衬线 |
| 导航、按钮 | 13–14px | 1.4–1.5 | 400 / 600–700，非衬线 |
| 元信息、标签、页脚 | 12–13px | 1.5 | 400，非衬线 |

- 默认标题为深蓝灰，正文为暖黑；不应将整个页面都写成纯黑或纯白。
- 英文标题可采用约 0.5px 字间距；中文正文默认不增加字间距。
- 日期、作者等辅助信息可使用微斜体，中文不强制合成斜体。
- 内容标题优先通过字阶、字重、细分隔线表现层级，不依赖字号突变。
- UI 字号应以 rem 或可缩放等效单位实现；12px 为默认最小视觉字号，不应限制用户放大。

## 7. 间距、布局与响应式

### 7.1 间距

以 4px 为基础构建间距序列，保留蓝本中 6、10、14、22px 等适合编辑排版的光学修正。

| 级别 | 默认值 | 使用场景 |
| --- | --- | --- |
| XS | 4–6px | 标签之间、标题与辅助信息 |
| S | 8–12px | 按钮内边距、紧密组件 |
| M | 14–16px | 内容段落、列表行 |
| L | 20–24px | 卡片内边距、栏间距 |
| XL | 28–32px | 主章节、封面和内容 |
| XXL | 40px | 主容器底部留白 |

### 7.2 网格

内容型页面默认是**居中的杂志式容器**，工具型页面可采用适应视口的面板布局。

| 参数 | 默认值 |
| --- | --- |
| 容器最大外宽 | 960px（含左右 padding，与源页面一致） |
| 容器水平内边距 | 20px |
| 容器顶部 / 底部内边距 | 28px / 40px |
| 导航高度 | 52px |
| 主内容与侧栏间距 | 24px |
| 侧栏宽度 | 280px |
| 卡片内边距 | 22px 24px |
| 卡片垂直间隔 | 22px |
| 头条封面参考高度 | 300px |

桌面双栏示意（最大容器时）：

```text
┌──────────────────── 深蓝灰导航栏 ────────────────────┐
│ 品牌                                             导航 │
└──────────────────────────────────────────────────────┘
       ┌────────────────── 封面 ──────────────────┐
       │                     图像 + 标题           │
       └───────────────────────────────────────────┘
       ┌───────────────────────┐  ┌──────────────┐
       │ 主内容 616px          │  │ 辅栏 280px   │
       │ 文章、列表、控制台    │  │ 分类、筛选   │
       └───────────────────────┘  └──────────────┘
                     24px 栏间距
```

布局宽度可按产品需要调整，例如信息密集的工具界面可以扩展至 1200px 或使用弹性工作区；但必须保留一致的间距、主次关系、结构边界与阅读节奏。

### 7.3 响应式

- 大于 760px：默认双栏；主栏使用弹性宽度，辅栏固定约 280px。
- 不大于 760px：改为单栏；辅栏完整移至主栏下方；封面标题约 22px。
- 窄屏可将外层内边距缩至 12–16px，卡片内边距缩至 16px。
- 移动端的导航必须改为可展开菜单或可访问的紧凑导航，不得像蓝本一样直接隐藏而无替代入口。
- 互动区域在触屏设备上应达到 44×44px；较小视觉控件可扩展实际命中区，避免相邻区域重叠。
- 320 CSS px 宽度及文本放大时，普通页面不应发生整页水平滚动。宽表格等内容允许独立滚动。

## 8. 组件规范（Components）

### 8.1 导航栏与应用工具栏

- 使用深蓝灰三段纵向渐变，1px 深色底边，顶部内高光及 E3 阴影。
- 品牌字标使用浅暖白衬线字体；琥珀点缀应保持小面积且满足可读性，若作为必要的文字，应使用更浅的高对比色。
- 导航项 13–14px、圆角 4px，普通状态浅灰文字；悬停为低透明度浅色填充。
- 当前项使用稳定底色或凹槽，并附带明晰标记（如加粗或下边标记）；不可只用悬停态表示当前页。
- 固定顶栏应给内容留出足够空间，避免遮挡被键盘聚焦的元素。

### 8.2 内容卡片（Card）

- 暖白纯色面、1px `border`、6px 圆角、E1 阴影，默认不作整卡渐变。
- 卡片标题与正文间使用 1px 暖灰实线；标题下可放日期、作者、类别等辅助信息。
- 同一层级卡片共享边界、内间距与阴影。静态卡片不要添加可点击的悬停变化。
- 列表类卡片可取消单个条目的独立背景，使用细分隔线组织密集内容。

### 8.3 按钮（Button）

| 类型 | 表面 | 语义 |
| --- | --- | --- |
| Primary | 琥珀三段渐变、深色文字、琥珀暗边 | 页面或流程的主操作 |
| Secondary | 浅暖灰渐变、深蓝灰文字、暖灰深边 | 次要操作 |
| Quiet | 无填充或低对比底色，保持文字操作可辨 | 低优先级操作、工具动作 |
| Destructive | 暗砖红渐变（如 `#A2382C → #83291F`）、浅色文字 | 删除等破坏性操作，使用明确动词 |

默认紧凑按钮 13–14px、600–700 字重，水平内边距 18px，垂直 8px，最小高度 36px；触屏应提高命中区。并非所有可点击文字都要制成凸起按钮。

| 状态 | 反馈 |
| --- | --- |
| Rest | 顶亮底暗、E2 阴影，清晰边界 |
| Hover | 表面略提亮，边界保持，过渡约 150ms |
| Focus-visible | 2px 高对比焦点环；不覆盖本体标签 |
| Active / Pressed | 反向或压平渐变，改为 I2 内阴影，外影消失 |
| Disabled | 暖灰低饱和表面、无动态高光；仍应能读出标签及禁用原因 |
| Loading | 保持控件尺寸，显示进度/等待文字或小型动画；避免重复提交 |

按下不应引起邻近布局位移。焦点、选中、悬停和按下是不同状态，不可混用。

### 8.4 表单（Input / Select / Textarea）

蓝本没有完整表单；LoMA 将其作为材质规则的扩展。

- 输入面使用暖白底、4–5px 圆角、可辨识的暖灰边界与 I1 内阴影，表现凹槽。
- 默认最小高度 36px（触屏命中区至少 44px）。正文标签放置在字段上方或左侧，不能仅用占位符代替。
- 下拉框的触发器沿用次级按钮材质；选择菜单使用暖白卡纸与 E4 阴影。
- 聚焦时使用焦点环；验证失败时同时显示砖红边缘、错误说明和图标。
- Placeholder 必须可辨但不可强过实际输入内容。
- 复选框与单选框使用可辨识边界、明确勾选/填充；选中可用琥珀色加深色符号。

### 8.5 标签、列表与表格

- **Tag：**默认 `surface-muted`，1px 边框，12px 圆角，轻微 1px 内亮边，12–13px 文字；内边距参考 3px 10px。选中/悬停可变为琥珀底深色字。
- **List：**每项纵向约 14px；使用 1px 虚线或细实线分隔，首末项去除不必要的外边距。标题可用 16px 粗衬线。
- **Table：**使用浅暖灰行表头、暖白背景、细分隔线和适度交替行色；数值列右对齐。操作按钮不应成为全表最抢眼的元素。
- **Tabs：**框架用浅暖灰材质，当前标签以暖白面或明确实体选中结构连接内容区；配合可访问的选中语义。

### 8.6 封面媒体（Hero）

- 使用 6px 圆角、边缘裁切、1px 低对比边框与 E4 阴影。
- 头条区域可采用图片、插画或蓝灰至暖褐的低饱和渐变，默认高约 300px。
- 文字可覆盖在底部深色渐变遮罩上：标题约 30px、白色或暖白，以 1–2px 文字阴影强化清晰度。
- 必须针对实际图片检查文字对比度。若遮罩不足，应增加实底标题带或调整文字位置；不可只依赖文字阴影。

### 8.7 图标、徽标与状态

- 常规图标优先简洁的原创线形或实心图形，16/20/24px 网格、约 1.5–2px 线宽。
- 对可按下的独立图标按钮，可使用小面积渐变、1px 内高光与短阴影；非交互图标保持平面感。
- 徽标、标签与状态以颜色、形状和文字共同表达。无文字图标按钮必须有可访问名称或清晰提示。
- 不混用厚重写实图标、高光球面图标与极细线图标；同一组使用同一视觉语法。

### 8.8 对话框、通知与进度（扩展）

- **Dialog：**暖白纸质面、6px 圆角、E4 阴影；可选深色标题框架；主操作使用琥珀按钮。遮罩应降低背景干扰，不使用背景模糊作为核心风格。
- **Notification：**依功能色制作淡色信息面，以细边、文字和图标传达状态；不需要强烈弹跳或闪烁。
- **Progress：**浅色凹槽 + 琥珀或蓝灰填充，顶部可有轻高光；不确定进度需有清晰等待提示。
- **Tooltip / Menu：**暖白边界与短柔影，必要时使用深蓝灰背景；显示和关闭方式须兼顾键盘操作。

### 8.9 页脚

暖灰色纵向渐变、1px 上边界、12–13px 辅助文字。页脚应是画布延伸而非深色导航的简单翻版。

## 9. 动效与交互反馈

| 动效 | 时间 | 规则 |
| --- | --- | --- |
| 按钮变色 / 光照变化 | 150ms | 短促，无延迟 |
| 导航及标签背景 | 150–200ms | 使用 ease-out 或 ease |
| 菜单、浮层 | 120–200ms | 淡入及小幅位移，幅度不宜超过 4px |
| 图标悬停 | 150ms | 可上移 1–2px，但不改变布局 |
| 按下 | 约 0–80ms | 优先即时反馈，避免等待动画完成 |

仅为颜色、透明度、阴影和小幅位移制作短过渡；避免无约束的 `transition: all`。不使用过长弹簧动画、鼠标追光或持续闪烁。尊重 `prefers-reduced-motion`，关闭非必要动画但保留状态变化；不要通过动画承担唯一的状态表达。

## 10. Web 实现参考

以下为从蓝本提炼并现代化的 CSS 起点，并非独立完整页面。其他平台（如 Godot 或桌面 UI）可以将同名令牌映射至主题资源、StyleBox、渐变纹理及控件状态；无需机械复刻 CSS 阴影实现。

### 10.1 核心令牌

```css
:root {
  /* Paper & surfaces */
  --loma-canvas: #e8e4dc;
  --loma-canvas-deep: #ddd8ce;
  --loma-surface: #fdfcf9;
  --loma-surface-muted: #f0ece3;
  --loma-border: #d6d0c4;
  --loma-divider: #e3ddd1;
  --loma-divider-dashed: #ddd6c8;

  /* Frame */
  --loma-slate-light: #4a5a6a;
  --loma-slate-mid: #35424f;
  --loma-slate-dark: #2b3642;
  --loma-slate-border: #1e262e;

  /* Accent & text */
  --loma-amber-light: #e8b04b;
  --loma-amber-mid: #d4942a;
  --loma-amber-dark: #c07f1a;
  --loma-amber-border: #a86a10;
  --loma-brick: #c0392b;
  --loma-brick-strong: #a2382c;
  --loma-text: #3a3a3a;
  --loma-text-body: #4a4a4a;
  --loma-text-muted: #736b60;
  --loma-text-on-canvas-muted: #625a4e;
  --loma-text-amber: #2c1b08;
  --loma-text-inverse: #f5f2ea;
  --loma-text-nav: #d8dde3;
  --loma-tag-text: #5a6a7a;
  --loma-focus: #28628a;

  /* Type */
  --loma-font-ui: "Helvetica Neue", Helvetica, Arial,
    "PingFang SC", "Microsoft YaHei", "Noto Sans CJK SC", sans-serif;
  --loma-font-heading: Georgia, "Times New Roman", "Songti SC",
    "Noto Serif CJK SC", SimSun, serif;
  --loma-font-mono: "SFMono-Regular", Consolas,
    "Liberation Mono", monospace;

  /* Shape & layout */
  --loma-radius-sm: 4px;
  --loma-radius-button: 5px;
  --loma-radius-card: 6px;
  --loma-radius-tag: 12px;
  --loma-container: 960px;
  --loma-side: 280px;
  --loma-gap: 24px;

  /* Surface gradients */
  --loma-frame: linear-gradient(to bottom,
    var(--loma-slate-light) 0%, var(--loma-slate-mid) 50%,
    var(--loma-slate-dark) 100%);
  --loma-primary: linear-gradient(to bottom,
    var(--loma-amber-light) 0%, var(--loma-amber-mid) 50%,
    var(--loma-amber-dark) 100%);
  --loma-primary-pressed: linear-gradient(to bottom,
    var(--loma-amber-dark) 0%, var(--loma-amber-mid) 50%,
    var(--loma-amber-light) 100%);
  --loma-secondary: linear-gradient(to bottom,
    #fdfcf9 0%, #f0ece3 55%, #e1dbd0 100%);

  /* Elevation */
  --loma-shadow-card: 0 1px 3px rgb(0 0 0 / 8%),
    0 4px 12px rgb(0 0 0 / 5%);
  --loma-shadow-button: inset 0 1px 0 rgb(255 255 255 / 40%),
    0 1px 2px rgb(0 0 0 / 20%);
  --loma-shadow-frame: inset 0 1px 0 rgb(255 255 255 / 15%),
    0 2px 4px rgb(0 0 0 / 20%);
  --loma-shadow-overlay: 0 1px 2px rgb(0 0 0 / 15%),
    0 6px 18px rgb(0 0 0 / 12%);
  --loma-shadow-inset: inset 0 1px 3px rgb(0 0 0 / 12%);
  --loma-shadow-pressed: inset 0 2px 4px rgb(0 0 0 / 25%);

  --loma-transition-fast: 150ms;
  --loma-transition-normal: 200ms;
}
```

### 10.2 基础组件 CSS

```css
*, *::before, *::after { box-sizing: border-box; }

body {
  margin: 0;
  font: 0.875rem/1.6 var(--loma-font-ui);
  color: var(--loma-text);
  background-color: var(--loma-canvas);
}
h1, h2, h3 {
  font-family: var(--loma-font-heading);
  color: var(--loma-slate-dark);
}
a { color: var(--loma-brick-strong); }
a:hover { text-decoration: underline; }

.loma-topbar {
  background: var(--loma-slate-mid);
  background-image: var(--loma-frame);
  color: var(--loma-text-inverse);
  border-bottom: 1px solid var(--loma-slate-border);
  box-shadow: var(--loma-shadow-frame);
}
.loma-topbar :is(h1, h2, h3) { color: inherit; }
.loma-topbar a { color: var(--loma-text-nav); }
.loma-container {
  max-width: var(--loma-container);
  margin-inline: auto;
  padding: 28px 20px 40px;
}
.loma-layout {
  display: grid;
  grid-template-columns: minmax(0, 1fr) var(--loma-side);
  gap: var(--loma-gap);
  align-items: start;
}
.loma-card {
  background: var(--loma-surface);
  border: 1px solid var(--loma-border);
  border-radius: var(--loma-radius-card);
  box-shadow: var(--loma-shadow-card);
  padding: 22px 24px;
}
.loma-card > h2 {
  margin: 0 0 8px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--loma-divider);
  font-size: 1.25rem;
}
.loma-meta {
  font-size: 0.75rem;
  color: var(--loma-text-muted); /* on surface */
}
.loma-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
  min-height: 36px;
  padding: 8px 18px;
  font: 700 0.8125rem/1.4 var(--loma-font-ui);
  text-decoration: none;
  color: var(--loma-text-amber);
  background: var(--loma-amber-light);
  background-image: var(--loma-primary);
  border: 1px solid var(--loma-amber-border);
  border-radius: var(--loma-radius-button);
  box-shadow: var(--loma-shadow-button);
  text-shadow: 0 1px 0 rgb(255 255 255 / 25%);
  cursor: pointer;
  transition: box-shadow var(--loma-transition-fast),
    border-color var(--loma-transition-fast);
}
.loma-button:hover:not(:disabled) {
  background-image: linear-gradient(to bottom,
    #f0bc58 0%, #dd9f36 50%, #c98a22 100%);
  text-decoration: none;
}
.loma-button:active:not(:disabled) {
  background-image: var(--loma-primary-pressed);
  box-shadow: var(--loma-shadow-pressed);
}
.loma-button--secondary {
  background: var(--loma-surface-muted);
  background-image: var(--loma-secondary);
  color: var(--loma-slate-dark);
  border-color: #8e8679;
}
.loma-button--secondary:hover:not(:disabled) {
  background-image: linear-gradient(to bottom, #fffefa, #e9e4da);
}
.loma-button--secondary:active:not(:disabled) {
  background-image: linear-gradient(to bottom, #e1dbd0, #fdfcf9);
}
.loma-button:disabled {
  background: #e2ded5;
  border-color: #b3aa9c;
  color: #625a4e;
  box-shadow: none;
  text-shadow: none;
  cursor: not-allowed;
}
.loma-input {
  min-height: 36px;
  max-width: 100%;
  padding: 8px 10px;
  font: inherit;
  color: var(--loma-text);
  background: var(--loma-surface);
  border: 1px solid #8e8679;
  border-radius: var(--loma-radius-sm);
  box-shadow: var(--loma-shadow-inset);
}
:focus-visible {
  outline: 2px solid var(--loma-focus);
  outline-offset: 2px;
}
.loma-topbar :focus-visible {
  outline-color: var(--loma-text-inverse);
}
@media (max-width: 760px) {
  .loma-layout { grid-template-columns: minmax(0, 1fr); }
  .loma-container { padding-inline: 16px; }
  .loma-card { padding: 16px; }
}
@media (pointer: coarse) {
  .loma-button, .loma-input { min-height: 44px; }
}
@media (prefers-reduced-motion: reduce) {
  .loma-button { transition: none; }
}
```

组件应优先使用语义化 HTML（button、a、input、nav、main 等）。CSS 类负责视觉，不替代状态语义和实际功能。不得仅为了样式把可交互元素改为没有键盘支持的 div。

## 11. 可访问性、扩展与一致性

### 11.1 可用性底线

- 普通文字与背景的对比度目标至少 4.5:1，大号文字至少 3:1；必要的非文本交互边界和状态标识应达到 3:1。
- 渐变表面要以文字所在的最不利颜色检验对比度，而不是只检查平均色或最亮色。
- 默认修正示例：深色琥珀按钮文字 `#2C1B08` 与渐变最暗端 `#C07F1A` 约为 4.96:1；卡片辅助文字 `#736B60` 与 `#FDFCF9` 约为 5.12:1。
- 不应以低对比的装饰分隔线充当必要的输入框边界。
- 所有交互组件必须具备可辨识的焦点、名称、状态和键盘操作方式；高对比/强制颜色模式应允许系统颜色覆盖。
- 页面信息不可只靠渐变方向、阴影、色彩或纹理传达；图标和文字要承担实际语义。
- 对真实项目的主题、图片、文字组合及全部状态逐一验证；本规范中的色板并不保证任意搭配都符合对比要求。

### 11.2 扩展策略

- 新增组件先确定语义角色，再匹配材质、几何、色彩、阴影等级，最后定义静态及交互状态。
- 主题品牌适配可置换琥珀强调色，但应维持暖纸与深色框架的主次关系，且重新检查对比度。
- 深色主题不是本版的现成配色映射。若新增深色 LoMA，应重新定义材质、明暗及文本层级，而非简单反转所有颜色。
- 可用于桌面、游戏和工具界面，但不要求强行复制网页的 960px 双栏结构。
- 新增设计令牌应具备语义名称，旧组件优先引用已有令牌，避免大量一次性硬编码色值。

## 12. 设计验收清单

### 视觉一致性

- [ ] 暖纸画布、暖白内容面、深蓝灰结构层与琥珀主操作件的主次明确。
- [ ] 纹理低于正文对比度，整体没有脏污、重噪点或过度做旧效果。
- [ ] 标题与正文的字体角色、字阶及间距清晰。
- [ ] 描边细而稳定，圆角以 4–6px 为主。
- [ ] 所有高光与阴影具有统一光照方向。
- [ ] 凸起控制件和凹入控制件拥有不同的视觉反馈。
- [ ] 内容面保持克制，不把每个区域都做成按钮式渐变。

### 功能与可用性

- [ ] 每个可操作组件拥有常态、悬停、焦点、按下及必要的禁用状态。
- [ ] 文字、必要边界与状态标识达到对比度目标。
- [ ] 键盘可到达、操作、关闭相关控件。
- [ ] 移动端导航完整，触屏命中区域足够，窄屏无无意义的整页横向滚动。
- [ ] 非必要动画可关闭，状态依然清晰。
- [ ] 放大字体时内容不被裁切，主次关系依旧成立。

### 实现维护

- [ ] 主要颜色、圆角、间距、阴影和渐变由主题令牌管理。
- [ ] 扩展组件沿用同一语义材质体系。
- [ ] 未使用与 LoMA 无关的大面积玻璃模糊、霓虹凸光或巨型圆角。
- [ ] 对自定义品牌变体和真实内容进行独立视觉验证。

---

## 13. 设计语言概述

LoMA 的核心不是「把现代网页做旧」，而是恢复界面中可感知的材料、边界、层级与操作手感。它以纸张承载信息，以深蓝灰建立结构，以琥珀形成行动信号；借助一致的光照、少量渐变、紧凑排版和克制细节，为数字界面赋予实体秩序与人文气质。

> **LoMA: design with the warmth of paper and the precision of an instrument.**  
> 以纸张的温度、器物的精确，设计数字界面。
