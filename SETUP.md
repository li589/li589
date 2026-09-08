# Profile README 部署说明（li589）

## 原理

GitHub 会把你**用户名同名仓库**（`li589/li589`）的 `README.md` 渲染显示在主页顶部。
所以只需要把这个 README 推到一个名为 `li589` 的公开仓库即可。

## 步骤

```bash
cd github-profile-li589

git init
git add README.md SETUP.md
git commit -m "Add profile README"

# 创建同名公开仓库并推送（你的 gh 已登录 li589 账号）
gh repo create li589 --public --source . --push
```

推送完成后访问 `https://github.com/li589` 即可看到效果。

## 需要你手动改的地方

1. **数据加载延迟**：统计卡片（github-readme-stats）需要账号有一定提交记录才丰满，刚开通时可能显示“暂无数据”，过一阵自动恢复。
2. **访客计数**：用的是 visitorbadge.io 免费服务，`path` 参数是自定义的，首次访问后才开始计数。

## 可选的后续增强

- **自动更新 README**：加一个 GitHub Actions，每天自动重写「最后更新」或插入博客文章 / WakaTime 统计。
- **换主题**：统计卡片 `theme=` 参数可换成 `dark` / `radical` / `tokyonight` 等；想换配色也可以告诉我，几分钟改好。
