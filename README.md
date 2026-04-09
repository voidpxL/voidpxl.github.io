
# voidpxL.github.io

这是 `voidpxL` 的个人主页仓库，基于 `Jekyll + GitHub Pages` 搭建，主要用于维护个人介绍、项目经历、成果展示和基础站点样式。

当前仓库里已经存在单独的 `/blog/` 页面与相关内容，但这份 README 主要面向“个人主页主站”的日常维护，不把 `/blog/` 作为默认修改范围。

站点地址：

- [https://voidpxl.github.io/](https://voidpxl.github.io/)

## 1. 工程用途

这个工程不是通用前后端项目，核心用途很直接：

- 展示个人简介、研究/工程方向和对外形象
- 展示项目经历、成果、奖项和其他补充信息
- 承载少量样式和导航定制
- 通过 GitHub Pages 进行静态部署

如果你后续继续维护，这个仓库更适合当作“个人主页内容仓库”理解，而不是“功能型网站工程”。

## 2. 主要目录说明

下面这些目录和文件是后续最常改的部分：

| 路径 | 作用 | 是否建议常改 |
| --- | --- | --- |
| `_config.yml` | 站点全局配置、作者信息、插件、SEO、头像路径等 | 是 |
| `_data/navigation.yml` | 顶部导航栏配置 | 是 |
| `_pages/about.md` | 首页入口页面，负责拼接各个内容模块 | 一般不常改结构时可改 |
| `_pages/includes/intro.md` | 个人简介 | 是 |
| `_pages/includes/portfolios.md` | 项目经历 | 是 |
| `_pages/includes/publications.md` | 成果/论文/输出 | 是 |
| `_pages/includes/awards.md` | 奖项信息 | 是 |
| `_pages/includes/others.md` | 其他补充内容 | 是 |
| `images/` | 头像、项目配图、favicon 等图片资源 | 是 |
| `assets/` | CSS、JS、字体等静态资源 | 偶尔 |
| `_sass/` | 站点样式细节 | 偶尔 |
| `.github/workflows/google_scholar_crawler.yaml` | Google Scholar 引用统计自动更新 | 按需 |
| `google_scholar_crawler/` | Scholar 抓取脚本 | 按需 |

默认不要把 `/blog/` 里的内容和主站个人介绍混在一起维护。主页是“静态能力和经历展示”，`/blog/` 更适合持续更新的轻量内容。

## 3. 本地运行

### 3.1 环境要求

- Ruby
- Bundler
- Git

如果本机还没装 Bundler，可以先执行：

```powershell
gem install bundler
```

### 3.2 安装依赖

在仓库根目录执行：

```powershell
bundle install
```

### 3.3 启动本地预览

推荐直接执行：

```powershell
bundle exec jekyll serve --livereload
```

然后打开：

- [http://127.0.0.1:4000](http://127.0.0.1:4000)

补充说明：

- 修改普通 Markdown、HTML、SCSS 后，Jekyll 通常会自动重新生成页面。
- 修改 `_config.yml` 后，通常需要重启本地服务。
- 仓库里虽然有 `run_server.sh`，但当前脚本写的是 `jekyll liveserve`，不要默认依赖它，优先使用上面的标准命令。

## 4. 常见修改入口

### 4.1 修改个人基本信息

优先改这两个地方：

- `_config.yml`
- `_pages/includes/intro.md`

常见内容包括：

- 站点标题
- 个人昵称
- 头像
- 简介
- 地点
- GitHub / ORCID / 邮箱等外链

### 4.2 修改首页内容结构

首页由 `_pages/about.md` 统一组织，里面通过 `include_relative` 拼接多个内容块。

如果只是改文案，通常改 `_pages/includes/*.md` 就够了。  
如果要新增一个主页板块，才需要同时修改：

- `_pages/about.md`
- `_pages/includes/新模块.md`
- `_data/navigation.yml`（如果需要导航入口）

### 4.3 修改项目经历

主要编辑：

- `_pages/includes/portfolios.md`
- `images/projects/`

建议每个项目至少包含：

- 项目名称
- 一句话目标
- 你负责的核心工作
- 使用的传感器/模型/部署平台
- 结果或价值
- 配图

不要只写“做了某系统”，这种信息密度太低，后面你自己回看也没价值。

### 4.4 修改成果、奖项和其他内容

分别编辑：

- `_pages/includes/publications.md`
- `_pages/includes/awards.md`
- `_pages/includes/others.md`

这几块建议保持“短、硬、可验证”，避免空泛描述。

### 4.5 修改导航栏

编辑：

- `_data/navigation.yml`

这里控制顶部菜单的标题和跳转地址。首页板块通常使用锚点，例如：

- `/#about-me`
- `/#portfolios`
- `/#publications`

### 4.6 修改样式

优先查看：

- `assets/css/main.scss`
- `_sass/`
- `_includes/head/custom.html`

建议先小改，不要一上来大面积重写主题。这个仓库本质上还是模板演化而来的 Jekyll 站点，粗暴改样式很容易牵一发动全身。

## 5. 后续维护建议

### 内容层面

- 个人简介保持简洁，重点突出你的主方向，而不是把所有经历堆上去
- 项目经历优先写“问题-方法-结果”，少写空泛口号
- 如果后续成果变多，优先做结构分组，不要把首页拉成一条很长的流水账
- 主站内容应偏稳定，频繁更新的思考记录更适合单独放到 `/blog/`

### 工程层面

- 每次改动后先本地预览，再提交
- 改 `_config.yml`、导航和样式时要重点检查首页是否有断链或错位
- 图片资源尽量压缩，避免主页加载太重
- 如果要继续用 Google Scholar 自动统计，记得维护 GitHub Actions 相关密钥

## 6. Google Scholar 自动更新

仓库里已经包含：

- `.github/workflows/google_scholar_crawler.yaml`
- `google_scholar_crawler/`

它的作用是定时抓取 Google Scholar 数据，并把结果推到 `google-scholar-stats` 分支。

如果后续要继续使用，需要确认：

- GitHub Actions 已启用
- 仓库 Secret 中配置了 `GOOGLE_SCHOLAR_ID`
- `_config.yml` 里相关作者字段配置正确

如果你并不依赖这套能力，可以先不折腾它，先把主页内容本身维护好。

## 7. 提交前自检

每次修改后，至少检查下面几项：

- 页面能否正常打开
- 导航锚点是否正确跳转
- 图片路径是否有效
- 中英文或编码是否出现乱码
- 移动端布局是否明显错位
- 修改是否误伤 `/blog/`

## 8. 建议的后续完善方向

如果后面继续迭代，这几个方向的收益通常更高：

1. 统一项目经历的写法，减少占位式描述
2. 补全成果页里的结构化信息，例如时间、角色、链接、摘要
3. 清理模板遗留内容，减少与当前个人主页无关的上游说明
4. 逐步把样式、内容和图片命名规范化，降低后续维护成本
5. 把首页内容控制在“信息密度高但不过载”的范围，不要堆砌

## 9. 备注

- `docs/README-zh.md` 更像是上游模板说明，不建议把它当作当前仓库的主维护文档。
- 当前真正应该看的入口文档，就是根目录这个 `README.md`。
