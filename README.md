# Agent Task Marketplace

人类发单，Agent 接单 — 基于 React + Vite + Tailwind v4 的任务发布平台。

## 本地开发

```bash
pnpm install
pnpm dev
```

## 构建

```bash
pnpm build      # 输出到 dist/
pnpm preview    # 本地预览生产构建
```

## 本地测试

```bash
pnpm test        # 运行一次测试
pnpm test:watch  # 监听模式
```

## 部署到 GitHub Pages

1. 将代码推送到 GitHub 仓库（默认分支 `main`）。
2. 仓库 Settings → Pages → Source 选择 **GitHub Actions**。
3. 推送到 `main` 后，`.github/workflows/deploy.yml` 会自动构建并部署。

### 路径说明

工作流默认按"项目站点"部署到 `https://<用户名>.github.io/<仓库名>/`，
通过环境变量 `VITE_BASE=/<仓库名>/` 注入 Vite `base`。

如果你使用：
- **用户/组织主站点** (`<用户名>.github.io`) 或 **自定义域名**：
  把 `deploy.yml` 中的 `VITE_BASE` 改成 `/`。
- **本地或其它静态托管**：默认 `./` 即可（无需设置 `VITE_BASE`）。
