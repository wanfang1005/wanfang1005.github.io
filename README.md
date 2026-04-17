# Wanfang's Learning Log

一个使用 Jekyll + Minimal Mistakes 主题的博客

## 📁 文章目录结构

```
├── _TestFramework/     # 测试框架相关
├── _Anthropology/      # 人类学笔记
├── _Language/          # 语言学习
├── _posts/             # 博客文章（可选）
└── 其他自定义分类...
```

## ✍️ 如何添加文章

### 1. 创建文章文件
在对应的分类文件夹中创建文件，命名格式：

```
YYYY-MM-DD-文章标题.md
```

示例：`_TestFramework/unit-test/2026-04-17-pytest.md`

### 2. 编写文章内容
```markdown
---
title: "Pytest 入门教程"
categories:
- TestFramework
- unit-test
tags:
- pytest
- python
---

# 正文内容开始

你的文章内容...
```

### 3. 添加新分类
在 `_config.yml` 中添加新的 collection：

```yaml
collections:
  YourCategory:
    title: "📂 分类名称"
    output: true
    permalink: /:collection/:path/
```

然后创建对应的文件夹：`_YourCategory/`

## 🔍 功能说明

- **侧边栏导航**：自动显示所有分类目录和标签
- **搜索功能**：支持按标题、内容、标签搜索
- **标签系统**：文章会自动归类到对应标签

## 🚀 本地运行

```bash
# 安装 Jekyll（如果还没安装）
gem install jekyll bundler

# 安装依赖
bundle install

# 启动本地服务器
bundle exec jekyll serve
# 或
jekyll serve

# 访问 http://localhost:4000
```

## 📝 注意事项

1. 所有文章必须以 `YYYY-MM-DD-` 开头
2. 每篇文章开头必须有 YAML front matter
3. 分类名称必须与 collection 名称匹配
4. 标签使用 `-` 分隔，如 `tags: [pytest, python]`

## 🎨 自定义

- 编辑 `_config.yml` 修改网站标题、描述等
- 编辑 `_data/navigation.yml` 调整侧边栏导航
- 编辑 `index.md` 自定义首页内容

---

*Happy blogging! 🚀*
