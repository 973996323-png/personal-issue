# 个人知识库 / Personal Issue

一个以 AI 通识学习为主线的个人内容仓库：Markdown 笔记 + 两个可直接打开的单文件网页。

> 🌐 在线访问：https://simmerfish.github.io/personal-issue/

## 目录结构

```
.
├── index.html             🌐 知识站首页（由 GitHub Pages 发布，可直接双击打开）
├── AI通识知识整理/        📚 主笔记（4 篇 Markdown + 目录导航 README）
├── AI通识知识笔记/        📝 早期整理稿（内容与主笔记有差异，保留作存档）
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

### 🌐 知识站（根目录 `index.html`）

把上面的笔记做成的**单文件静态网站**（内联 CSS/JS，无外部依赖、无需构建）：从「晶体管到机器人」的图文通识站，含自测题与延伸学习路径。

放在仓库**根目录**，是为了让 GitHub Pages 能直接把它作为首页发布（Pages 选 `main` 分支 + `/`(root) 即可）。

**本地预览**：直接双击 `index.html`，或

```bash
python3 -m http.server 8000
# 打开 http://localhost:8000
```

**发布**：整站只有一个文件，任意静态托管都可直接用（GitHub Pages / Cloudflare Pages / surge / Vercel…）。

> 📌 2025 年做过两次结构调整：删除了该站的 `CNAME`（内容为 `ai-tongshi.surge.sh`，是 surge.sh 的发布域名残留）；原 `AI通识知识站/` 目录已取消，`index.html` 上提到根目录。若将来要绑定自定义域名，在根目录新建 `CNAME` 写入自己的域名即可。

### 🧪 `test-web/`

页面效果实验，与知识站相互独立。

## 日常使用

```bash
git add -A
git commit -m "docs: 更新内容"
git push
```

本仓库通过 SSH 推送（`~/.ssh/id_ed25519` → `git@github.com:simmerfish/personal-issue.git`）。

## 忽略规则

见 `.gitignore`：忽略 `.DS_Store`、`.env*`、`node_modules/`、`dist/`、`*.log`。

---

**作者**：szy · 内容主要整理自 AI 学习过程中的对话与阅读笔记，仅供学习参考。
