<div align="center">
<img src="docs/assets/hero.svg" width="100%" alt="lucide-icon-plus — 创业路上要补的描边图标" />
</div>

<div align="center">
<pre>~/lucide-icon-plus (main*)  0 plus icons  24px stroke</pre>
</div>

<div align="center">

[![English](https://img.shields.io/badge/lang-EN-8b949e?style=for-the-badge&labelColor=0d1117)](README.md)
[![中文](https://img.shields.io/badge/lang-ZH-0E2951?style=for-the-badge&labelColor=0d1117)](README.zh-CN.md)

</div>

## lucide-icon-plus

创业路上 Lucide 还没有的描边图标。

— 同一套 24×24 描边。用 Lucide 的引擎。上游图标保持原样。

[![license](https://img.shields.io/badge/license-MIT-0E2951?style=flat-square)](LICENSE)
[![grid](https://img.shields.io/badge/grid-24x24-0E2951?style=flat-square)](docs/assets/hero.svg)
[![stroke](https://img.shields.io/badge/stroke-2px_round-555555?style=flat-square)](README.zh-CN.md)
[![engine](https://img.shields.io/badge/engine-lucide-0E2951?style=flat-square)](https://github.com/lucide-icons/lucide)
[![upstream](https://img.shields.io/badge/upstream-untouched-555555?style=flat-square)](README.zh-CN.md)

一套公开的 plus 图标，描边和 Lucide 一致，补公司在做成之前每块界面缺的那一枚。

**Tips for getting started**

1. 先读下面的图标契约，再动笔。
2. 缺的图标放进 `icons/<name>.svg`。
3. Lucide 已经发布的图标继续从 lucide 引入。这个仓库只增加 plus 集。

---

## 定位

| | |
| --- | --- |
| **谁** | 界面已经在用 Lucide，又缺一枚创业场景图标 |
| **做什么** | 按 Lucide 的描边把这枚图标画出来，再用 Lucide 的图标构建编译 |
| **边界** | Lucide 现有图标留在 Lucide 仓库里，不修改 |

## 流水线

```text
缺的一笔
    → icons/<name>.svg      24×24，描边 2，圆头
    → Lucide 图标构建       只吃本仓库的文件
    → 和 lucide 一起引入    已有图标仍来自 lucide
```

| 步骤 | 做什么 | 闸门 |
| --- | --- | --- |
| 1. 确认缺口 | 某个界面需要 Lucide 里没有的描边 | Lucide 已有的，直接用 Lucide |
| 2. 绘制 | 在 24 网格上新增 `icons/<name>.svg` | `fill="none"`，描边宽度 2，圆头圆角 |
| 3. 构建 | 把这套图标交给 Lucide 的图标构建 | 构建输入是这里的 `icons/`，不是改过的 Lucide 目录 |
| 4. 使用 | plus 图标和 Lucide 原有图标一起引入 | 发布出去的 Lucide 包保持原发布内容 |

## 仓库布局

| 路径 | 作用 |
| --- | --- |
| `icons/` | plus 的 SVG。第一枚图标落地时建立这个目录 |
| `docs/assets/hero.svg` | README 头图 |
| `LICENSE` | MIT，版权 jqu224 |

## 契约

| 规则 | 含义 |
| --- | --- |
| 画布 | `viewBox="0 0 24 24"`，`fill="none"`，`stroke="currentColor"`，`stroke-width="2"`，圆头圆角 |
| 命名 | 一个文件一个 kebab-case 名字。Lucide 已经发布过的名字不加 |
| 上游 | 不拷贝、不改名、不修改 Lucide 仓库里的图标 |
| 引擎 | 用 Lucide 的图标构建来编译 plus 集。描边风格保持 Lucide 的 |

```xml
<svg
  xmlns="http://www.w3.org/2000/svg"
  width="24"
  height="24"
  viewBox="0 0 24 24"
  fill="none"
  stroke="currentColor"
  stroke-width="2"
  stroke-linecap="round"
  stroke-linejoin="round"
>
  <path d="..." />
</svg>
```

## 用法

| 动作 | 做法 |
| --- | --- |
| 加一枚图标 | 按上面的契约新建 `icons/<name>.svg` |
| 用 Lucide 的引擎 | 让 Lucide 的图标构建读取本仓库的 `icons/` |
| 用 Lucide 已有图标 | 从 `lucide` 引入，不要放进 `icons/` |
| 数量 | 这棵树里目前是 `0` 枚 plus 图标 |

## 许可证

[MIT](LICENSE)
