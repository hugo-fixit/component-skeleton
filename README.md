<!-- markdownlint-disable-file MD033 MD041 -->
<h1 align="center">{component-xxx} | FixIt</h1>

<!-- TODO 如有需要，请在此处添加图片 -->

<div align="center" class="ignore">
  <p><!-- TODO 如有需要，请在此处添加描述 --></p>
  简体中文 |
  <a href="https://fixit.lruihao.cn/zh-cn/ecosystem/hugo-fixit/{component-xxx}/?lang=chinese_traditional">繁體中文</a> |
  <a href="/README.en.md">English</a> |
  <a href="https://fixit.lruihao.cn/ecosystem/hugo-fixit/{component-xxx}/?lang=french">Français</a> |
  <a href="https://fixit.lruihao.cn/ecosystem/hugo-fixit/{component-xxx}/?lang=russian">Русский язык</a> |
  <a href="https://fixit.lruihao.cn/ecosystem/hugo-fixit/{component-xxx}/?lang=spanish">Español</a> |
  <a href="https://fixit.lruihao.cn/ecosystem/hugo-fixit/{component-xxx}/?lang=hindi">हिन्दी</a> |
  <a href="https://fixit.lruihao.cn/ecosystem/hugo-fixit/{component-xxx}/?lang=german">deutsch</a> |
  <a href="https://fixit.lruihao.cn/ecosystem/hugo-fixit/{component-xxx}/?lang=korean">한국어</a> |
  <a href="https://fixit.lruihao.cn/ecosystem/hugo-fixit/{component-xxx}/?lang=japanese">しろうと</a>
</div>

## Demo

TODO 如有需要，请在此处添加演示

## 特性

- [ ] Foo
- [ ] Bar

## 要求

- FixIt v0.3.12 或更高版本。

## 安装组件

安装方式与 [安装主题](https://fixit.lruihao.cn/zh-cn/documentation/installation/) 相同，有多种安装方式，任选一种即可，这里介绍两种主流方式。

### 作为 Hugo 模块安装

首先确保你的项目本身是一个 [Hugo 模块](https://gohugo.io/hugo-modules/use-modules/#initialize-a-new-module)。

然后将此主题组件添加到你的 `hugo.toml` 配置文件中：

```toml
[module]
  [[module.imports]]
    path = "github.com/hugo-fixit/FixIt"
  [[module.imports]]
    path = "github.com/hugo-fixit/{component-xxx}"
```

在 Hugo 的第一次启动时，它将下载所需的文件。

要更新到模块的最新版本，请运行：

```bash
hugo mod get -u
hugo mod tidy
```

### 作为 Git 子模块安装

将 [FixIt](https://github.com/hugo-fixit) 和此 git 存储库克隆到你的主题文件夹中，并将其作为网站目录的子模块添加。

```bash
git submodule add https://github.com/hugo-fixit/FixIt.git themes/FixIt
git submodule add https://github.com/hugo-fixit/{component-xxx}.git themes/{component-xxx}
```

接下来编辑项目的 `hugo.toml` 并将此主题组件添加到你的主题中：

```toml
theme = ["FixIt", "{component-xxx}"]
```

## 配置

为了通过 FixIt 主题在 `layouts/partials/custom.html` 文件中开放的 [自定义块](https://fixit.lruihao.cn/references/blocks/) 将 `{component-xxx}.html` 注入到 `custom-assets` 中，你需要填写以下必要配置：

```toml
[params]
  [params.customPartials]
    head = []
    profile = []
    aside = []
    comment = []
    footer = []
    widgets = []
    assets = [
      "inject/{component-xxx}.html",
    ]
    postFooterBefore = []
    postFooterAfter = []
```

TODO 如有需要，请在此处添加配置...

## 使用 Shortcode

以下是一个使用示例：

```markdown
{{< shortcode-xxx >}}
```

## 参考

- [开发主题组件 | FixIt](https://fixit.lruihao.cn/contributing/components/)
- [如何开发 Hugo 主题组件 | FixIt](https://fixit.lruihao.cn/components/dev-component/)
