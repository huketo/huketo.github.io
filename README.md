# Hugo FixIt Blog Template (Go)

👉 한국어 | [English](README.en.md) | [简体中文](README.cn.md)

이것은 Hugo theme [FixIt](https://github.com/hugo-fixit/FixIt) 의 빠른 시작 템플릿입니다. [Hugo Modules](https://gohugo.io/hugo-modules/) 기능을 사용하여 테마를 불러오고 있습니다.

기본 테마 구조와 설정파일이 제공됩니다. GitHub action을 사용하여 GitHub page에 자동으로 배포되도록 설정되어 있습니다. 또한 매일 자정에 자동으로 테마를 업데이트하는 cron 작업도 설정되어 있습니다.

## Directory structure

```bash
▸ .github/       # GitHub configuration
▸ archetypes/    # page archetypes (like scaffolds of archetypes)
▸ assets/        # css, js, third-party libraries etc.
▸ config/        # configuration files
▸ content/       # markdown files for hugo project
▸ data/          # blog data (allow: yaml, json, toml), e.g. friends.yml
▸ public/        # build directory
▸ static/        # static files, e.g. favicon.ico
▸ themes/        # theme submodules
▸ go.mod
▸ go.sum
```

## Quick Start

자세한 빠른 시작 가이드는 이 [page](https://fixit.lruihao.cn/documentation/getting-started/)를 참조하세요.

### Prerequisites

- [Go](https://go.dev/dl/)
- [Hugo](https://gohugo.io/installation/): >= 0.112.0 (extended version)

### Use Template

> 이 레포지토리는 Template가 아니므로 설명만 기재합니다.

1. **Use this template** 버튼을 클릭해 Github에서 repository를 생성하세요.

<img width="913" alt="image" src="https://github.com/hugo-fixit/hugo-fixit-starter1/assets/33419593/d5fbd940-3ffd-4750-b1e6-4e87b50b0696">

2. 다음으로 repository가 생성되었다면, clone 하면 됩니다(--recursive 포함).

   ```bash
   # Clone with your own repository url
   git clone --recursive https://github.com/<your_name>/<your_blog_repo>.git
   ```

### Launching the Site

```bash
# Development environment
hugo server
# Production environment
hugo server -e production
```

### Build the Site

사이트를 배포할 준비가 되었다면, 이 커맨드를 실행하세요:

```bash
hugo
```

### Update Theme

나중에 이 명령어를 사용하여 테마를 업데이트할 수 있습니다:

```bash
# Update theme manually
hugo mod get -u github.com/hugo-fixit/FixIt@latest
hugo mod tidy
```

<details>
  <summary>Start via NPM script</summary>

```bash
# build the blog
npm run build
# run a local debugging server with watch
npm run server
# run a local debugging server in production environment
npm run server:production
# update theme submodules
npm run update:theme
```

</details>

## Troubleshooting

<details>
  <summary>remote: Permission to git denied to github-actions[bot].</summary>
  Head to Setting => Actions => General => Workflow permissions => Check "Read and write permissions".
</details>

<!-- This project was generated with [hugo-fixit-starter](https://github.com/hugo-fixit/hugo-fixit-starter). -->
