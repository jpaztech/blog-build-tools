# Example

This is example CSS blog.

## Init/Update [blog theme](https://github.com/jpazureid/hexo-theme-jpazure) submodule

```shell
git submodule update -i
```

## Run/Stop Hexo server

```shell
docker-compose up

# Ctrl+C
docker-compose down
```

## Directory structure

```
example
├── .github
│   └── workflows
│       └── pages.yml  # Workflow definition for GitHub Action
├── .gitignore
├── .textlintrc
├── README.md
├── _config.yml        # Site configration
├── articles           # Blog articles
│   └── information
│       └── test.md    # Example post
├── docker-compose.yaml    # Configuration for container to run locally
├── github-issue-template.md
├── scaffolds
├── source
└── themes             # Blog themes
    └── jpazure (git submodule)
```
