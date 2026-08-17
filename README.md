# 王若愚的个人主页

这是一个部署在 GitHub Pages 上的静态个人网站。站点使用 Jekyll 4 构建，内容按「学术、文字、音乐」三个栏目组织；样式基于本仓库维护的 Hacker 主题 Sass 源码。

## 项目结构

| 路径 | 用途 |
| --- | --- |
| `_config.yml` | 站点元数据、集合（collections）与默认布局配置。 |
| `_layouts/`、`_includes/`、`_data/` | 页面骨架、导航组件与导航数据。 |
| `_research/`、`_research_thoughts/` | 学术栏目及学术随想。 |
| `_writing/`、`_writing_essays/`、`_writing_fictions/`、`_writing_poetry/`、`_writing_readings/` | 文字栏目、分类页和各类文章。 |
| `_music/`、`_music_sheets/` | 音乐栏目和曲谱页面。 |
| `_sass/`、`assets/css/style.scss` | 主题样式和站点自定义样式；使用 Dart Sass 的 `@use` 模块语法。 |
| `assets/` | 图片、音频、曲谱等静态资源。 |
| `_site/` | Jekyll 本地构建产物，不应手动编辑或提交。 |

集合与布局的对应关系由 `_config.yml` 中的 `defaults` 统一维护：栏目首页使用 `research`、`writing` 或 `music` 布局，具体文章使用相应的 `*_posts` 布局。

## 环境要求

- Ruby 3.2 或更高版本；当前 `Gemfile.lock` 锁定的 Bundler 4.0.18 要求 Ruby 3.2+。
- RubyGems 和 Bundler 4.0.18。

确认环境：

```sh
ruby --version
bundle --version
```

如果没有合适的 Bundler，请安装锁定版本：

```sh
gem install bundler -v 4.0.18
```

Ruby 的安装方式可按操作系统和个人工具链选择（系统包、mise、asdf、rbenv 等）。无需执行 `bundle init`，仓库已包含 `Gemfile` 与 `Gemfile.lock`。

## 安装依赖

在仓库根目录执行：

```sh
bundle config set --local path vendor/bundle
bundle install
```

第一条命令将依赖安装在项目内的 `vendor/bundle`，避免污染系统 Ruby 环境；该目录和 Bundler 本地配置均不会提交到仓库。后续依赖变更应通过 `Gemfile` 与 `Gemfile.lock` 管理，而不是全局安装 Jekyll。

## 本地开发

启动开发服务器：

```sh
bundle exec jekyll serve
```

访问 <http://127.0.0.1:4000> 预览站点。Jekyll 会监视源文件并自动重新生成页面；按 `Ctrl-C` 停止服务。

仅构建并检查生成是否成功：

```sh
bundle exec jekyll build
```

生成文件位于 `_site/`。始终使用 `bundle exec`，以确保命令运行在 `Gemfile.lock` 锁定的依赖版本中。

## 添加和维护内容

1. 在对应的集合目录新增 Markdown 文件。文章文件建议使用 `YYYY-MM-DD-标题.md` 命名，以便文章布局显示正确日期。
2. 添加 YAML front matter；至少填写 `title`。文章可按需添加 `subtitle`、`tags`、`excerpt` 与 `usemathjax`。布局由 `_config.yml` 自动分配，通常无需手动填写 `layout`。
3. 将图片、音频和曲谱分别放在 `assets/images/`、`assets/audios/`、`assets/sheets/`，并使用相对站点路径引用。
4. 如需新栏目或导航项，同时更新 `_config.yml`、相应的 `_data/navi*.yml`，以及需要展示该栏目的索引页面。
5. 提交前运行 `bundle exec jekyll build`，并在本地检查相关页面、链接和静态资源。

普通页面同样使用 Markdown 和 front matter；网站首页是 `index.md`。导航数据位于 `_data/navi.yml`、`_data/navi_research.yml`、`_data/navi_writing.yml` 与 `_data/navi_music.yml`。

## 样式维护

站点主题源码已本地化在 `_sass/`，入口文件为 `assets/css/style.scss`。修改样式后运行本地服务器或构建命令即可生成 `assets/css/style.css`。新增 Sass 依赖时使用 `@use`，不要重新引入已弃用的 `@import` 语法。
