# 个人知识库 / Personal Issue

一个以 AI 通识学习为主线的个人内容仓库：Markdown 笔记 + 两个可直接打开的单文件网页。

## 目录结构

```
.
├── AI通识知识整理/        📚 主笔记（4 篇 Markdown + 目录导航 README）
├── AI通识知识笔记/        📝 早期整理稿（内容与主笔记有差异，保留作存档）
├── AI通识知识站/          🌐 单文件知识站网页（index.html，可直接双击打开）
└── test-web/              🧪 页面实验（Claude Code 介绍页，index.html）
```

### 📚 `AI通识知识整理/`

从零基础视角串联机器人、大模型与芯片的完整笔记，6 篇约 12 万字（含图）。

- `README.md` — 总目录与导读（推荐从这里进入）
- `AI通识知识整理.md` — 主稿
- `AI与芯片知识整理.md` / `AI与芯片通识知识.md` — 芯片与硬件底层的展开
- `AI通识知识笔记.md` — 原始笔记

### 📝 `AI通识知识笔记/`

早期版本的 `AI通识知识整理.md`。与主笔记**内容不完全相同**（各自独立演进），因此单独保留而非删除，避免丢失历史结论。

### 🌐 `AI通识知识站/`

把上面的笔记做成的**单文件静态网站**（内联 CSS/JS，无外部依赖、无需构建）：从「晶体管到机器人」的图文通识站，含自测题与延伸学习路径。

**本地预览**：直接双击 `index.html`，或

```bash
python3 -m http.server 8000 --directory AI通识知识站
# 打开 http://localhost:8000
```

**发布**：整站只有一个文件，任意静态托管都可直接用（GitHub Pages / Cloudflare Pages / surge / Vercel…）。

> 该目录原先带一个 `CNAME`（内容为 `ai-tongshi.surge.sh`），2025 年已删除。它属于 surge.sh 的发布域名残留，若将来启用 GitHub Pages 并绑定自定义域名，再新建 `CNAME` 写入自己的域名即可。

### 🧪 `test-web/`

页面效果实验，与知识站相互独立。

## 日常使用

```bash
git add -A
git commit -m "docs: 更新内容"
git push
```

本仓库通过 SSH 推送（`~/.ssh/id_ed25519` → `git@github.com:973996323-png/personal-issue.git`）。

## 忽略规则

见 `.gitignore`：忽略 `.DS_Store`、`.env*`、`node_modules/`、`dist/`、`*.log`。

---

**作者**：szy · 内容主要整理自 AI 学习过程中的对话与阅读笔记，仅供学习参考。
