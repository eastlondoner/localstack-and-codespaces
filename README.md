# localstack-and-codespaces

Simple example GitHub codespace that includes localstack and the AWS cli.

## codespaces configuration

The `.devcontainer/` directory contains the codespaces configuration and has its own README.

### Quick start

[Create your own codespace](https://docs.github.com/en/codespaces/developing-in-codespaces/creating-a-codespace) for this repository.

Run the examples from the `examples/` directory to test interacting with localstack.

### Changing the base image 

Currently devcontainer.json is set to use the `mcr.microsoft.com/vscode/devcontainers/universal:linux` container image as the basis of the codespace environment. This [universal image](https://github.com/microsoft/vscode-dev-containers/tree/main/containers/codespaces-linux) contains dependencies for development with a range of popular languages like Python, Node, PHP, Java, Go, C++, Ruby, Go, Rust and .NET Core/C#. 

There are many other pre-built images that you can choose from for common tasks. The [Microsoft VS Code Docker Hub repository](https://hub.docker.com/_/microsoft-vscode-devcontainers) is a good place to find available containers. To use a different base image change the value of `build.args.BASE_IMAGE` in `.devcontainer/devcontainer.json` to the image that you want to use.

N.b. Only Debian or Ubuntu based images will work with the build scripts in `.devcontainer/build`

For example:

 - nodejs `"BASE_IMAGE": "mcr.microsoft.com/vscode/devcontainers/javascript-node:16-buster"`
 - go `"BASE_IMAGE": "mcr.microsoft.com/vscode/devcontainers/go:1.17-buster"`
 - python  `"BASE_IMAGE": "mcr.microsoft.com/vscode/devcontainers/python:3.9-buster"`
