# File/templates — PersonalPortfolio

这个目录是 File 数据结构的参考模板区。它的作用是说明“实际内容目录应该怎么放”，并给出每类文件的填写样例。

## 实际 File 结构

```text
File/
├── achievements/
│   └── achievements.yml
├── assets/
├── cv/
├── profile/
│   ├── about-me.md
│   ├── hero.md
│   └── profile.yml            # 可选
├── projects/
│   ├── projects.yml
│   ├── air-calling-landing-page/
│   │   └── description.md      # 可选
│   ├── business-landing-page/
│   │   └── description.md      # 可选
│   └── ecom-web-page/
│       └── description.md      # 可选
├── services/
│   ├── icons/
│   └── services.yml
├── templates/
│   ├── README.md
│   ├── about.md
│   ├── achievements.yml
│   ├── profile.yml
│   ├── project-description.md
│   ├── projects.yml
│   ├── services.yml
│   └── testimonials.yml
└── testimonials/
	├── avatars/
	└── testimonials.yml
```

## 存储规则

### 1. 结构化数据使用 YAML
适合“列表、索引、配置”这类数据。

- `File/projects/projects.yml`：项目列表
- `File/services/services.yml`：服务列表
- `File/testimonials/testimonials.yml`：推荐语列表
- `File/achievements/achievements.yml`：成就列表
- `File/profile/profile.yml`：个人信息配置（可选）

### 2. 内容化数据使用 Markdown
适合“正文、长描述、详细介绍”这类内容。

- `File/profile/about-me.md`：个人介绍
- `File/profile/hero.md`：首页主视觉文案
- `File/projects/<id>/description.md`：单个项目的详细说明
- `File/testimonials/<id>/text.md`：推荐语正文（较长时使用）
- `File/achievements/<id>/text.md`：成就说明（较长时使用）

### 3. 图片、附件放在对应子目录
媒体文件不要混到 YAML 里，统一放在对应条目的子目录或资源目录中。

- `File/projects/<id>/cover.jpg`
- `File/projects/<id>/spec.pdf`
- `File/services/icons/icon.svg`
- `File/testimonials/avatars/avatar.jpg`
- `File/assets/`：通用静态资源
- `File/cv/resume.pdf`：简历文件

## 模板文件说明

- `projects.yml`：项目模板
- `services.yml`：服务模板
- `testimonials.yml`：推荐模板
- `achievements.yml`：成就模板
- `profile.yml`：个人配置模板
- `about.md`：关于我正文模板
- `project-description.md`：项目正文模板

## 使用建议
1. 先看 `projects.yml`，它最能说明结构化数据怎么写。
2. 长文本放 Markdown，短列表放 YAML。
3. 新项目先建子目录，再补图片、附件和正文文件。
4. 所有相对路径都以 `File/` 为根目录来写。
