# 🚀 GitHub Pages 托管与发布高智感作品集指南

本指南将手把手带您将本地的交互式作品集（包括主页 `index.html`、多主题预览页 `themes.html` 以及黑客帝国版 `matrix.html`）免费部署到 **GitHub Pages** 上，让面试官通过公网随时随地流畅访问。

---

## 🗺️ 两种部署方案（任选其一）

根据您期望的公网网址（URL）样式，选择适合您的部署策略：

### 🎯 方案 A：发布为您的“个人主页主域名”（推荐 ⭐⭐⭐⭐⭐）
*   **网址效果**：`https://<您的用户名>.github.io/`
*   **优势**：地址最简短、高级，适合作为个人招牌。
*   **仓库命名**：新建仓库名称必须完全等于您的用户名，即 `<您的用户名>.github.io`。

### 📦 方案 B：发布为“子项目路径域名”
*   **网址效果**：`https://<您的用户名>.github.io/portfolio/`
*   **优势**：如果您还想建立其他独立项目，这是一种模块化的管理方式。
*   **仓库命名**：新建仓库名称命名为任意词，例如：`portfolio`。

---

## 🛠️ 第一步：在 GitHub 上新建空白仓库

1.  打开浏览器，访问 [GitHub New Repository 页面](https://github.com/new)。
2.  填写信息：
    *   **Repository name（仓库名称）**：
        *   *如果走方案 A*：填写 `lockstock.github.io`（或者如果您目前的账号还是 `cyang8319-png`，则填写 `cyang8319-png.github.io`）。
        *   *如果走方案 B*：填写 `portfolio`。
    *   **Visibility（可见性）**：必须选择 **Public**（公开，私有仓库无法使用免费版 GitHub Pages）。
    *   **初始化选项**：⚠️ **不要**勾选 "Add a README file"、"Add .gitignore" 或 "Choose a license"。保持这是一个**完美的空仓库**。
3.  点击底部的 **Create repository**。

---

## 💻 第二步：在本地终端（Terminal）上传您的网页代码

打开您的 Mac Terminal 终端，运行以下命令，将本地 `portfolio` 文件夹中的所有精美网页文件一次性推送到 GitHub 上。

```bash
# 1. 进入您的作品集本地文件夹
cd "/Users/chengyang/Documents/HARDDRIVE/1. Job Hunting/Resumes/portfolio"

# 2. 初始化本地 Git 仓库
git init

# 3. 将本地所有网页文件、特效文件加入暂存区
git add .

# 4. 提交本地版本库
git commit -m "feat: deploy premium portfolio suites (Default, Theme Switcher, Matrix Mode)"

# 5. 切换默认分支为 main
git branch -M main

# 6. 关联您刚刚在 GitHub 新建的远程仓库 (请根据您的实际用户名替换 <your-username> 和 <repo-name>)
# 例如：git remote add origin https://github.com/lockstock/lockstock.github.io.git
git remote add origin https://github.com/<your-username>/<repo-name>.git

# 7. 强力推送代码到 GitHub 远程端
git push -u origin main -f
```

---

## ⚙️ 第三步：在 GitHub 网页端激活 Pages 部署

1.  代码推送成功后，刷新您在 GitHub 上的仓库页面，您会看到所有的网页文件（`index.html`, `themes.html`, `matrix.html`）已经就位。
2.  点击页面上方的 ⚙️ **Settings**（设置）选项卡。
3.  在左侧边栏中找到 **Code and automation** 模块，点击 **Pages**。
4.  在 **Build and deployment** 下的 **Source** 中，保持选择为 **Deploy from a branch**（从分支部署）。
5.  在 **Branch** 栏中：
    *   将 `None` 改选为 **`main`** 分支。
    *   旁边的目录保持选择为 **`/ (root)`**。
    *   点击 **Save**（保存）按钮。

---

## 🎉 第四步：公网发布成功与访问

稍等 30 秒至 1 分钟，GitHub Pages 会在后台完成自动化云编译。

1.  刷新当前 Pages 设置页面，您会看到顶部亮起绿色的横幅：
    > **Your site is live at `https://<your-username>.github.io/...`**
2.  点击该链接即可公网查阅。

### 🔗 您的专属云端矩阵导航矩阵：
*   **极简原配主页**：`https://<your-username>.github.io/index.html`（或直接访问根目录）
*   **多配色一键切换页**：`https://<your-username>.github.io/themes.html`
*   **黑客帝国特攻操作台**：`https://<your-username>.github.io/matrix.html`

> [!IMPORTANT]
> **联动更新**：
> 当您发布成功后，记得将您 [GitHub Profile README 模板](file:///Users/chengyang/.gemini/antigravity/brain/82930bed-f909-4cd6-8dda-5dd0899cac6a/github_profile_readme.md) 顶部的 `INTERACTIVE PORTFOLIO` 徽章链接，更新为您的真实 GitHub Pages 线上公网网址！
