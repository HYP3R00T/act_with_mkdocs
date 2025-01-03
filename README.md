# `act` with `mkdocs`

This is a sample repo to test github action pipeline locally using act.

## References

- [Act](https://github.com/nektos/act)
- [Github Action Documentation](https://docs.github.com/en/actions)
- [MkDocs Material](https://github.com/squidfunk/mkdocs-material)

## How to Install it Locally?

While `act` is available for some platforms, it's easy to use the `curl` command.

```bash
cd ~
curl --proto '=https' --tlsv1.2 -sSf https://raw.githubusercontent.com/nektos/act/master/install.sh | sudo bash
```

When we install it, it will create a `bin` folder in the current working directory. So, it's recommended to change directory to home. Also, add the `bin` directory to the path.

## How to Use `act` to Test GitHub Action Pipeline?

### Prerequisites

- Docker: Make sure docker is installed and the engine is running before using `act`.
- Use git (VCS) in your project.

### Execution

- Create a pipeline in `.github/workflows` directory.
- Presuming you only have one pipeline for now, simply run `act` from the terminal, in your project directory.

It will use Docker to pull all required images and run the pipeline locally.

## The Problem

There is no other tool or method to test the pipeline before committing the changes to GitHub. While `act` is working, it's still very limited.
