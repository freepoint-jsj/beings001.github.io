
# Gmeek 初始化包（freepoint-jsj）

这是为 **虚妄之相的文字馆** 准备的可直接导入的初始化文件。

## 目录
- `config.json`：站点配置 + 首页/文章页的定制样式（极简 V2EX 风格卡片）
- `.github/workflows/Gmeek.yml`：自动构建与部署工作流（GitHub Actions）

## 使用步骤（一次性）
1. 打开你的仓库：`freepoint-jsj/freepoint.github.io`。
2. 进入 **Settings → Pages**，把 **Build and deployment → Source** 设为 **GitHub Actions**。
3. 把本包的 **`config.json`** 放到仓库根目录，**`.github/workflows/Gmeek.yml`** 放到 `.github/workflows/` 目录（缺了就新建同名文件夹）。
4. 在仓库的 **Actions** 页找到 **build Gmeek**，点击 **Run workflow**（全局生成一次）。
5. 写第一篇文章：打开 **Issues**，新建 Issue，**一定要给它添加至少 1 个 Label**，保存后等构建完成，访问 `https://freepoint-jsj.github.io/`。

> 修改了 `config.json` 后，请在 **Actions → build Gmeek → Run workflow** 手动触发一次“全局生成”。

## 常见问题
- **首页没内容/只显示标题时间**：因为文章 Issue 没有加 Label。给每篇 Issue 添加 1 个 Label，重新生成即可。
- **构建失败**：一般是 `config.json` 格式错误或未全局生成。先检查 JSON 最后一行不要逗号，然后去 Actions 手动 Run 一次。
- **作者邮箱（提交签名）**：已设置为 `freepoint-jsj@users.noreply.github.com`，如需改成你自己的邮箱，修改 `config.json` 的 `email`。

祝写作顺利。
