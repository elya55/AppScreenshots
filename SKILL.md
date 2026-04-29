---
name: appscreen
description: Use when generating App Store or Google Play marketing screenshots from raw app captures. Smarter than generic: Vision-based auto-analysis first, 5-question intake (not 15), Chinese/English bilingual copy, 5 named design styles, mascot/IP support, auto screenshot renaming. Triggers on: app store screenshots, 应用市场截图, 应用商店宣传图, store listing images, marketing screenshots.
---

# AppScreen — 应用商店截图生成器

## 核心哲学

**截图是广告，不是说明书。** 每张截图只卖一个感受或结果。用视觉说服，用文字确认。

**工作流程：分析截图 → 5问答 → 确认文案 → 搭建项目 → 构建 → 导出**

---

## Phase 0：Vision 智能分析（收到截图后立即执行，不要先问问题）

用户发来截图后，**第一步不是问问题，而是分析**。

### 0.1 对每张截图做视觉分析

判断并记录：

| 维度 | 要判断的内容 |
|------|------------|
| **屏幕类型** | home / onboarding / feature / chat / ai / list / settings / celebration / empty |
| **主色调** | 背景色 + 主要 UI 颜色（近似 hex）|
| **内容关键词** | 这个界面展示的核心功能/内容 |
| **情绪基调** | calm / playful / focused / social / rewarding |
| **推荐叙事角色** | hero / differentiator / feature / trust / summary |

### 0.2 自动输出分析报告

格式如下（直接给用户看，不要藏起来）：

```
📊 截图分析完成

| # | 类型 | 检测内容 | 推荐故事角色 |
|---|------|---------|------------|
| 1 | [屏幕类型] | [检测到的界面内容] | [Hero / Differentiator / Feature / Trust / Summary] |
| 2 | [屏幕类型] | [检测到的界面内容] | [Hero / Differentiator / Feature / Trust / Summary] |
| 3 | [屏幕类型] | [检测到的界面内容] | [Hero / Differentiator / Feature / Trust / Summary] |
| N | [屏幕类型] | [检测到的界面内容] | [Hero / Differentiator / Feature / Trust / Summary] |

🎨 检测品牌色：[主色 hex]（颜色名）/ [背景色 hex]（颜色名）/ [辅色 hex]（颜色名）
📐 推荐幻灯顺序：[最优叙事顺序，如 1 → 3 → 2 → 4]
💡 推荐张数：[N] 张（基于截图数量和内容丰富度）
```

**以上是输出格式模板。实际内容完全基于用户上传的截图，由 Vision 分析得出，不得使用任何预设内容。**

然后立即进入 Phase 1 提问。

---

## Phase 1：最小化问答（5 个问题，一次性列出）

```
分析完成！只需回答 5 个问题，我就能直接开始：

1. APP 名称是什么？
2. 目标平台：App Store / Google Play / 两个都要？
3. 文案语言：中文 / 英文 / 中英双语？
4. 要几张宣传图？（推荐 X 张，基于分析）
5. 视觉风格选一个：
   · warm-playful   温暖可爱（奶油色+自然绿，适合角色IP类）
   · clean-minimal  干净极简（白底几何，工具类/效率类）
   · dark-premium   深色高级（深底+光晕，科技/游戏/财务）
   · gradient-vivid 渐变鲜艳（强饱和渐变，社交/娱乐/年轻化）
   · flat-pastel    马卡龙扁平（粉嫩治愈，健康/生活/女性向）

可选：有 APP 图标吗？有品牌 IP 形象吗？
```

**不确定的项目，用户可以说"你来决定"，我根据截图风格自主判断。**

---

## Phase 2：幻灯叙事框架与文案

### 2.1 叙事弧线框架

根据张数自动适配：

| 张数 | 叙事结构 |
|------|---------|
| 3 | Hero → 核心功能 → 总结/品牌 |
| 4 | Hero → 差异化 → 核心功能 → 总结 |
| 5 ★ | Hero → 情感差异化 → 功能特色 → 反馈/成就 → 品牌总结 |
| 6 | Hero → 差异化 → 功能A → 功能B → 反馈 → 总结 |
| 7-8 | 在中间扩展更多功能幻灯，最后一张必须是深色对比/总结 |

**规则：**
- 第1张（Hero）是最重要的，大多数用户只看这张
- 倒数第2张或最后1张做成深色对比，制造视觉节奏
- 总结张不放截图，只放 App Icon + 功能胶囊

### 2.2 文案铁律

**不管中文还是英文，必须遵守：**
1. 每张幻灯只卖一个核心价值
2. 标题在手机缩略图尺寸下 1 秒内可读
3. 禁止用 "and" / "和" 并联两个卖点
4. 不用营销废话："全新"、"智能AI"、"一键"、"强大"

**中文版专属规则：**
- 标题：每行 3-6 个汉字
- 副标题：8-14 个汉字
- 句式优先：动词开头（"感受"、"找到"、"告别"、"开始"）
- 避免直白功能名（"查看每日情绪统计" → "知道自己今天的感受"）

**英文版专属规则：**
- 标题：每行 3-5 个单词
- 禁止标题里用 "and"
- 推荐动作结果型（"Feel better." / "Stay on track." / "Never miss a day."）

**双语版：** 中英文各自独立创作，不是直译。同一张幻灯中英文可用不同角度切入同一个卖点。

### 2.3 文案输出格式

为每张幻灯生成 **3 套选项**，格式：

```
[幻灯1 — Hero]

选项A（结果型）：
  中：[基于该APP核心价值，动词开头，3-6字]
  英：[Outcome-first, 3-5 words per line.]

选项B（时刻型）：
  中：[描述用户使用该APP的具体时刻，4-8字]
  英：[Paint a moment the user pictures themselves doing.]

选项C（痛点型）：
  中：[点名用户使用该APP之前的痛点，4-8字]
  英：[Name a problem this app destroys.]

★ 推荐：选项[X]（[推荐理由，一句话，说明为何最短最直接最符合该APP调性]）
```

**所有文案选项完全基于用户 APP 的实际功能和截图内容生成，不得套用与该 APP 无关的文案。**

**在用户确认文案后再开始写代码。**
如果用户说"你来决定"，自选最佳选项直接进入构建。

---

## Phase 3：项目搭建

### 3.1 包管理器检测（优先级：bun > pnpm > yarn > npm）

```bash
which bun && echo "bun" || which pnpm && echo "pnpm" || which yarn && echo "yarn" || echo "npm"
```

### 3.2 脚手架

```bash
# npm（最常见）
npx create-next-app@latest . --typescript --tailwind --app --src-dir --no-eslint --import-alias "@/*" --yes
npm install html-to-image

# bun（更快）
bunx create-next-app@latest . --typescript --tailwind --app --src-dir --no-eslint --import-alias "@/*" --yes
bun add html-to-image
```

⚠️ **目录名不能有大写字母。** 如果当前目录名有大写（如 AppScreenshots），在父目录创建：
```bash
# 父目录执行
npx create-next-app@latest myapp-screenshots --typescript --tailwind --app --src-dir --no-eslint --import-alias "@/*" --yes
```

### 3.3 资源整理（必须做，防止文件名混乱）

```bash
mkdir -p public/screenshots

# 将截图统一重命名为 01.png, 02.png... 避免大小写和空格问题
cp /path/to/screenshot1.png public/screenshots/01.png
cp /path/to/screenshot2.png public/screenshots/02.png
# ...

# 复制其他资源
cp /path/to/app-icon.png public/app-icon.png
cp /path/to/mascot.png public/mascot.png      # 有IP形象时
cp ~/.claude/skills/appscreen/mockup.png public/mockup.png
```

**统一使用 `01.png, 02.png` 命名，永远不要在代码里写 `1.png` 或原始文件名。**

### 3.4 文件结构

```
project/
├── public/
│   ├── mockup.png          # iPhone 框架（从 skill 目录复制）
│   ├── app-icon.png        # APP 图标
│   ├── mascot.png          # IP 形象（可选）
│   └── screenshots/
│       ├── 01.png          # 统一零填充命名
│       ├── 02.png
│       └── ...
└── src/app/
    ├── layout.tsx          # 字体配置
    └── page.tsx            # 单文件生成器
```

---

## Phase 4：构建页面

### 4.1 layout.tsx — 字体配置

根据风格和语言选择字体：

| 风格 | 英文字体 | 中文字体（双语时） |
|------|---------|-----------------|
| warm-playful | Nunito | Noto Sans SC |
| clean-minimal | Inter | Noto Sans SC |
| dark-premium | Space Grotesk | Noto Sans SC |
| gradient-vivid | Poppins | Noto Sans SC |
| flat-pastel | Nunito | Noto Sans SC |

```tsx
// 纯英文
import { Nunito } from "next/font/google";
const font = Nunito({ subsets: ["latin"], weight: ["400","500","600","700","800","900"] });

// 双语（中文主导）
import { Noto_Sans_SC } from "next/font/google";
const font = Noto_Sans_SC({ subsets: ["chinese-simplified"], weight: ["400","500","700","900"] });
```

### 4.2 page.tsx — 架构

**整个生成器是单一 page.tsx，不拆分文件，不建 API routes。**

```
page.tsx 结构
├── "use client";
├── 常量（画布尺寸、Frame 测量值、导出尺寸）
├── THEME 设计系统（根据用户选择的风格）
├── 图片路径数组 + preloadAllImages()
├── img() 辅助函数
├── phoneW() 宽度计算
├── Phone 组件（iPhone frame）
├── Slide1 ~ SlideN（每张幻灯独立函数）
├── ScreenshotPreview（ResizeObserver 缩放预览）
└── ScreenshotsPage（工具栏 + 网格 + 批量导出）
```

### 4.3 核心常量

```typescript
// 画布：iPhone 6.9"（最大尺寸，导出时缩放至其他尺寸）
const W = 1320, H = 2868;

// iPhone mockup 预测量值（固定，不可更改）
const MK_W = 1022, MK_H = 2082;
const SC_L  = (52   / MK_W) * 100;
const SC_T  = (46   / MK_H) * 100;
const SC_W  = (918  / MK_W) * 100;
const SC_H  = (1990 / MK_H) * 100;
const SC_RX = (126  / 918)  * 100;
const SC_RY = (126  / 1990) * 100;
const MK_RATIO = MK_W / MK_H;

// 导出尺寸
const IPHONE_SIZES = [
  { label: '6.9"', w: 1320, h: 2868 },
  { label: '6.5"', w: 1284, h: 2778 },
  { label: '6.3"', w: 1206, h: 2622 },
  { label: '6.1"', w: 1125, h: 2436 },
] as const;
```

### 4.4 五大设计风格（THEMES）

```typescript
const THEMES = {
  "warm-playful": {
    // 背景渐变
    bg: (dark?: boolean) => dark
      ? "linear-gradient(170deg, #0C1E0F 0%, #162A1A 50%, #0F2214 100%)"
      : "linear-gradient(155deg, #F6F1EA 0%, #EAF5EA 100%)",
    // 文字色
    headline: (dark?: boolean) => dark ? "#F5F0E8" : "#1A2615",
    sub:      (dark?: boolean) => dark ? "rgba(245,240,232,0.6)" : "#527B48",
    label:    "#52C06B",
    // 装饰
    glow:     (dark?: boolean) => dark
      ? "rgba(82,192,107,0.28)"
      : "rgba(82,192,107,0.22)",
    // 胶囊颜色
    pills: ["#52C06B","#4A90D9","#C87A00","#9B7FD4","#E8845A","#50C8B4"],
  },
  "clean-minimal": {
    bg: (dark?: boolean) => dark
      ? "linear-gradient(180deg, #0D0D0D 0%, #1A1A2E 100%)"
      : "linear-gradient(180deg, #FFFFFF 0%, #F4F5F7 100%)",
    headline: (dark?: boolean) => dark ? "#FFFFFF" : "#0D0D0D",
    sub:      (dark?: boolean) => dark ? "rgba(255,255,255,0.5)" : "#666666",
    label:    (dark?: boolean) => dark ? "#AAAAAA" : "#444444",
    glow:     (dark?: boolean) => dark ? "rgba(255,255,255,0.06)" : "rgba(0,0,0,0.04)",
    pills: ["#1A1A2E","#333","#555","#777","#999","#BBB"],
  },
  "dark-premium": {
    bg: () => "linear-gradient(145deg, #0A0A14 0%, #111128 100%)",
    headline: () => "#F0EEFF",
    sub:      () => "rgba(240,238,255,0.55)",
    label:    "#9D92FF",
    glow:     (dark?: boolean) => dark
      ? "rgba(124,111,255,0.35)"
      : "rgba(124,111,255,0.22)",
    pills: ["#7C6FFF","#4ECDC4","#FF6B9D","#FFD93D","#6BCB77","#4D96FF"],
  },
  "gradient-vivid": {
    bg: (dark?: boolean) => dark
      ? "linear-gradient(135deg, #B71C1C 0%, #E65100 100%)"
      : "linear-gradient(135deg, #FF6B6B 0%, #FFA726 100%)",
    headline: () => "#FFFFFF",
    sub:      () => "rgba(255,255,255,0.80)",
    label:    "rgba(255,255,255,0.95)",
    glow:     () => "rgba(255,255,255,0.15)",
    pills: ["rgba(255,255,255,0.95)","rgba(255,255,255,0.80)","rgba(255,255,255,0.65)",
            "rgba(255,255,255,0.50)","rgba(255,255,255,0.38)","rgba(255,255,255,0.25)"],
  },
  "flat-pastel": {
    bg: (dark?: boolean) => dark
      ? "linear-gradient(150deg, #2D1B33 0%, #1A1028 100%)"
      : "linear-gradient(150deg, #FFF0F5 0%, #E8F4FE 100%)",
    headline: (dark?: boolean) => dark ? "#FFE4EE" : "#2D1B33",
    sub:      (dark?: boolean) => dark ? "rgba(255,228,238,0.6)" : "#7A5A8A",
    label:    "#FF8FAB",
    glow:     (dark?: boolean) => dark ? "rgba(255,143,171,0.3)" : "rgba(255,143,171,0.2)",
    pills: ["#FF8FAB","#74C0FC","#63E6BE","#FFD43B","#B197FC","#FF922B"],
  },
} as const;

type ThemeId = keyof typeof THEMES;
const [themeId] = useState<ThemeId>("warm-playful"); // 根据用户选择替换默认值
const theme = THEMES[themeId];
```

**如果用户的品牌色与选定风格不符，提取用户品牌色覆盖 label 和 glow 值。**

### 4.5 图片预加载（必须，否则导出黑屏）

```typescript
const IMAGE_PATHS = [
  "/mockup.png",
  "/app-icon.png",
  // 有IP形象时加："/mascot.png",
  "/screenshots/01.png",
  "/screenshots/02.png",
  // ... 所有截图
];

const imageCache: Record<string, string> = {};

async function preloadAllImages() {
  await Promise.all(IMAGE_PATHS.map(async (path) => {
    try {
      const r = await fetch(path);
      const blob = await r.blob();
      const dataUrl = await new Promise<string>((res) => {
        const reader = new FileReader();
        reader.onloadend = () => res(reader.result as string);
        reader.readAsDataURL(blob);
      });
      imageCache[path] = dataUrl;
    } catch { console.warn("Preload failed:", path); }
  }));
}

function img(path: string): string { return imageCache[path] || path; }
```

**在 useEffect 里调用，ready 状态门控渲染：**
```typescript
const [ready, setReady] = useState(false);
useEffect(() => { preloadAllImages().then(() => setReady(true)); }, []);
if (!ready) return <LoadingState />;
```

### 4.6 Phone 组件（iPhone frame）

```tsx
function Phone({ src, alt, style }: { src: string; alt: string; style?: React.CSSProperties }) {
  return (
    <div style={{ position: "relative", aspectRatio: `${MK_W}/${MK_H}`, ...style }}>
      <img src={img("/mockup.png")} alt="" style={{ display: "block", width: "100%", height: "100%" }} draggable={false} />
      <div style={{
        position: "absolute", zIndex: 10, overflow: "hidden",
        left: `${SC_L}%`, top: `${SC_T}%`, width: `${SC_W}%`, height: `${SC_H}%`,
        borderRadius: `${SC_RX}% / ${SC_RY}%`,
      }}>
        <img src={src} alt={alt} style={{ display: "block", width: "100%", height: "100%", objectFit: "cover", objectPosition: "top" }} draggable={false} />
      </div>
    </div>
  );
}
```

### 4.7 宽度计算函数

```typescript
function phoneW(cW: number, cH: number, clamp = 0.84) {
  return Math.min(clamp, 0.72 * (cH / cW) * MK_RATIO);
}
// 用于两机并排的小尺寸
function phoneW2(cW: number, cH: number) { return phoneW(cW, cH, 0.64); }
```

用法：`width: \`${phoneW(cW, cH) * 100}%\``

### 4.8 排版系统（所有尺寸相对 cW，自动适配导出分辨率）

| 元素 | 英文大小 | 中文大小 | 字重 | 行高 |
|------|---------|---------|------|------|
| Label（小标签）| `cW * 0.028` | `cW * 0.026` | 700 | — |
| Sub（副标题）| `cW * 0.037` | `cW * 0.035` | 500 | 1.45 |
| Headline（主标题）| `cW * 0.095` | `cW * 0.105` | 900 | 0.93 |
| 功能胶囊文字 | `cW * 0.033` | `cW * 0.030` | 600 | — |

*中文字号调大是因为汉字视觉密度高于拉丁字母。*

### 4.9 幻灯布局规则

**每张幻灯的必备元素：**
1. 渐变背景 + 至少一个 glow 光晕装饰
2. Label（小标签）+ Headline（主标题）+ Sub（副标题）
3. 截图放入 Phone 组件（总结幻灯除外）
4. 一个视觉变化元素（IP 形象 / 几何装饰 / 额外 glow）

**手机位置模式（相邻幻灯不得重复）：**

```
居中沉入底部（Hero 标准）：
  bottom: 0, left: "50%", transform: "translateX(-50%) translateY(12%)"

偏右居中：
  bottom: 0, left: "54%", transform: "translateX(-50%) translateY(12%)"

偏左居中：
  bottom: 0, left: "46%", transform: "translateX(-50%) translateY(12%)"

两机叠加（比较/生态场景）：
  后：left: "-8%", width: phoneW2*100%, rotate(-4deg), opacity: 0.5
  前：right: "-4%", width: phoneW*100%, translateY(10%)

无手机（总结幻灯）：
  只有 App Icon + 标题 + 功能胶囊，不放截图
```

**深色对比幻灯：** 每套至少 1 张（放倒数第2位），最多 2 张。
**warm-playful / flat-pastel** 风格的深色版：使用各自 theme 的 dark 参数。

### 4.10 IP 形象 / 吉祥物使用规范

如果用户提供了 mascot.png：

```tsx
// Companion 幻灯（右上角浮动，品牌识别）
<img src={img("/mascot.png")} style={{
  position: "absolute", top: "6%", right: "5%",
  width: cW * 0.18, zIndex: 25,
  filter: "drop-shadow(0 4px 16px rgba(0,0,0,0.15))",
}} draggable={false} />

// 总结幻灯（居中大图，替代 App Icon）
<img src={img("/mascot.png")} style={{
  width: cW * 0.35, marginBottom: cW * 0.04,
  filter: "drop-shadow(0 8px 24px rgba(0,0,0,0.15))",
}} draggable={false} />
```

**不要在所有幻灯都放 IP 形象，1-2 张点缀即可，避免视觉疲劳。**

### 4.11 总结幻灯（无截图，品牌收尾）

```tsx
function SlideSummary({ cW, cH }: { cW: number; cH: number }) {
  const features = ["功能A", "功能B", "功能C", "功能D", "功能E", "功能F"];
  return (
    <div style={{
      width: "100%", height: "100%", position: "relative", overflow: "hidden",
      background: theme.bg(),
      display: "flex", flexDirection: "column", alignItems: "center", justifyContent: "center",
    }}>
      {/* Center glow */}
      <div style={{
        position: "absolute", top: "40%", left: "50%", transform: "translate(-50%,-50%)",
        width: "75%", height: "65%",
        background: `radial-gradient(circle, ${theme.glow()} 0%, transparent 68%)`,
      }} />
      {/* App Icon */}
      <img src={img("/app-icon.png")} style={{
        width: cW * 0.2, height: cW * 0.2, borderRadius: cW * 0.044,
        marginBottom: cW * 0.05, position: "relative", zIndex: 10,
        boxShadow: `0 ${cW*0.016}px ${cW*0.055}px ${theme.glow()}`,
      }} draggable={false} />
      {/* Headline — 根据用户APP填写，如"还有更多"/"And so much more." */}
      <div style={{
        fontSize: cW * 0.09, fontWeight: 900,
        color: theme.headline(), lineHeight: 0.93, textAlign: "center",
        position: "relative", zIndex: 10, marginBottom: cW * 0.022,
      }}>
        {SUMMARY_HEADLINE}
      </div>
      {/* Sub — 根据用户APP一句话价值主张填写 */}
      <div style={{
        fontSize: cW * 0.035, color: theme.label, fontWeight: 700,
        marginBottom: cW * 0.065, position: "relative", zIndex: 10,
      }}>
        {SUMMARY_SUB}
      </div>
      {/* Feature pills */}
      <div style={{
        display: "flex", flexWrap: "wrap", justifyContent: "center",
        gap: cW * 0.022, width: "78%", position: "relative", zIndex: 10,
      }}>
        {features.map((f, i) => (
          <div key={f} style={{
            padding: `${cW*0.016}px ${cW*0.04}px`,
            borderRadius: cW * 0.06,
            background: theme.pills[i % theme.pills.length] + "1A",
            border: `${cW*0.003}px solid ${theme.pills[i % theme.pills.length]}55`,
            fontSize: cW * 0.031, fontWeight: 600,
            color: theme.pills[i % theme.pills.length],
            whiteSpace: "nowrap",
          }}>{f}</div>
        ))}
      </div>
    </div>
  );
}
```

### 4.12 工具栏布局（Export 按钮永远可见）

```tsx
<div style={{ position: "sticky", top: 0, zIndex: 50, background: "white", borderBottom: "1px solid #e5e7eb", display: "flex", alignItems: "center" }}>
  {/* 可滚动控制区 */}
  <div style={{ flex: 1, display: "flex", alignItems: "center", gap: 12, padding: "12px 20px", overflowX: "auto", minWidth: 0 }}>
    <img src="/app-icon.png" style={{ width: 28, height: 28, borderRadius: 7, flexShrink: 0 }} />
    <span style={{ fontWeight: 800, fontSize: 15, whiteSpace: "nowrap" }}>APP名 · Screenshots</span>
    <select value={sizeIdx} onChange={e => setSizeIdx(Number(e.target.value))}
      style={{ fontSize: 12, border: "1px solid #e5e7eb", borderRadius: 6, padding: "5px 10px", fontFamily: "inherit" }}>
      {IPHONE_SIZES.map((s, i) => <option key={i} value={i}>{s.label} — {s.w}×{s.h}</option>)}
    </select>
  </div>
  {/* 固定 Export 按钮 */}
  <div style={{ flexShrink: 0, padding: "12px 20px", borderLeft: "1px solid #e5e7eb" }}>
    <button onClick={exportAll} disabled={!!exporting} style={{
      padding: "8px 22px", background: exporting ? "#93c5fd" : "#52C06B",
      color: "white", border: "none", borderRadius: 8,
      fontSize: 13, fontWeight: 700, cursor: exporting ? "default" : "pointer",
      whiteSpace: "nowrap", fontFamily: "inherit",
    }}>
      {exporting ? `导出中 ${exporting}…` : "导出全部"}
    </button>
  </div>
</div>
```

### 4.13 ScreenshotPreview（ResizeObserver 缩放）

```tsx
function ScreenshotPreview({ slide, index, cW, cH, exportRef }) {
  const previewRef = useRef<HTMLDivElement>(null);
  const [scale, setScale] = useState(1);

  useEffect(() => {
    if (!previewRef.current) return;
    const ro = new ResizeObserver(([entry]) => {
      const { width, height } = entry.contentRect;
      setScale(Math.min(width / cW, height / cH));
    });
    ro.observe(previewRef.current);
    return () => ro.disconnect();
  }, [cW, cH]);

  return (
    <div style={{ display: "flex", flexDirection: "column", gap: 8 }}>
      {/* 预览 */}
      <div ref={previewRef} style={{
        width: "100%", aspectRatio: `${cW}/${cH}`,
        overflow: "hidden", borderRadius: 12,
        boxShadow: "0 4px 20px rgba(0,0,0,0.12)", position: "relative",
      }}>
        <div style={{ width: cW, height: cH, transform: `scale(${scale})`, transformOrigin: "top left", position: "absolute" }}>
          <slide.Comp cW={cW} cH={cH} />
        </div>
      </div>
      {/* 导出用隐藏副本 */}
      <div ref={exportRef} style={{ width: cW, height: cH, position: "absolute", left: "-9999px", top: 0, opacity: 0 }}>
        <slide.Comp cW={cW} cH={cH} />
      </div>
      <div style={{ textAlign: "center", fontSize: 12, color: "#888", fontWeight: 600 }}>
        {String(index + 1).padStart(2, "0")} — {slide.id}
      </div>
    </div>
  );
}
```

---

## Phase 5：导出系统

### 5.1 导出函数（双调用，缺一不可）

```typescript
import { toPng } from "html-to-image";

async function captureSlide(el: HTMLElement, w: number, h: number): Promise<string> {
  el.style.left = "0px";
  el.style.opacity = "1";
  el.style.zIndex = "-1";

  const opts = { width: w, height: h, pixelRatio: 1, cacheBust: true };
  await toPng(el, opts);               // 第一次：预热字体和图片（结果丢弃）
  const dataUrl = await toPng(el, opts); // 第二次：实际输出

  el.style.left = "-9999px";
  el.style.opacity = "0";
  el.style.zIndex = "";
  return dataUrl;
}
```

### 5.2 批量导出

```typescript
async function exportAll() {
  const size = IPHONE_SIZES[sizeIdx];
  for (let i = 0; i < SLIDES.length; i++) {
    setExporting(`${i + 1}/${SLIDES.length}`);
    const el = exportRefs.current[i].current;
    if (!el) continue;
    const dataUrl = await captureSlide(el, size.w, size.h);
    const a = document.createElement("a");
    a.href = dataUrl;
    a.download = `${String(i + 1).padStart(2, "0")}-${SLIDES[i].id}-${size.w}x${size.h}.png`;
    a.click();
    await new Promise(r => setTimeout(r, 300));
  }
  setExporting(null);
}
```

### 5.3 导出关键规则

| 规则 | 原因 |
|------|------|
| 必须双调用 toPng | 第一次预热字体/图片，第二次才清晰 |
| 导出前移至 left:0 | 屏幕外元素不渲染 |
| 外层 overflowX: hidden | 防止导出元素造成横向滚动 |
| 所有图片用 img() helper | 防止非确定性 fetch 导致黑色矩形 |
| 文件名零填充前缀 | 排序正确：01, 02...10 |
| 单次导出后 delay 300ms | 防止浏览器节流 |

---

## Phase 6：质检清单

在发布给用户前自查：

### 文案质量
- [ ] 每张幻灯只卖一个核心价值
- [ ] Hero 幻灯 1 秒内可读，主标题不超过 2 行
- [ ] 没有"和/and"并联两个卖点
- [ ] 中文标题不超过 6 字/行

### 视觉质量
- [ ] 相邻幻灯手机位置不重复（左/中/右/无手机轮换）
- [ ] 全套至少 1 张深色对比幻灯
- [ ] 装饰元素不遮挡截图关键内容
- [ ] 品牌色/Label 色全套一致

### 导出质量
- [ ] Export All 按钮固定在工具栏右侧，不随内容滚动消失
- [ ] 文件名零填充排序正确
- [ ] 导出不黑屏、不白屏（双调用 + preload）
- [ ] 截图无黑色矩形（img() helper）

---

## 常见问题速查

| 现象 | 原因 | 修复 |
|------|------|------|
| 导出全黑/白屏 | 未双调用 toPng；或元素仍在 -9999px | 确保双 toPng + 导出前 left:0 |
| 手机屏幕黑色矩形 | 图片未 preload 为 dataURL | 所有图用 img() helper |
| 字体不渲染 | Google Fonts 首次加载慢 | 双调用自动解决（第一次预热）|
| 横向滚动出现 | 导出元素超出视口 | 外层加 overflowX: "hidden" |
| 截图顺序混乱 | 文件名大小写/空格 | 统一重命名为 01.png, 02.png |
| create-next-app 报错 | 目录名含大写字母 | 在父目录创建小写名子目录 |
| 中文字体显示为方框 | Nunito 不含 CJK | 改用 Noto Sans SC |
| 幻灯1截图不对 | 文件下载顺序与预期不符 | 先 `file public/screenshots/*.png` 确认内容，再写路径 |

---

## 交付说明

构建完成后，向用户说明：

1. **叙事弧线**：简述每张幻灯的故事逻辑
2. **对比幻灯**：指出哪张是深色对比幻灯及其位置意图
3. **文案选择**：说明最终选择哪套文案及理由
4. **运行命令**：
   ```bash
   npm run dev   # 启动
   # 打开 http://localhost:3000
   # 选择导出尺寸 → 点击"导出全部"
   ```
5. **后续定制**：说明如何修改（改颜色在 THEMES，改文案在 SlideN 函数）
