# Harmon Boilerplates

My boilerplates for various stacks such as Docker Compose, Ansible, Terraform, shell scripts, etc.

Author: Evan Harmon

[![Validate](https://github.com/evanharmon1/harmon-boilerplates/actions/workflows/validate.yml/badge.svg)](https://github.com/evanharmon1/harmon-boilerplates/actions/workflows/validate.yml)
[![Build](https://github.com/evanharmon1/harmon-boilerplates/actions/workflows/build.yml/badge.svg)](https://github.com/evanharmon1/harmon-boilerplates/actions/workflows/build.yml)
[![Security](https://github.com/evanharmon1/harmon-boilerplates/actions/workflows/security.yml/badge.svg)](https://github.com/evanharmon1/harmon-boilerplates/actions/workflows/security.yml)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border-orange.json)](https://github.com/copier-org/copier)
[![Maintained](https://img.shields.io/badge/maintained%3F-yes-brightgreen.svg?style=flat-square)](https://github.com/evanharmon1/harmon-boilerplates)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat-square)](https://github.com/evanharmon1/harmon-boilerplates)
[![Known Vulnerabilities](https://snyk.io/test/github/evanharmon1/harmon-boilerplates/badge.svg?style=flat-square)](https://snyk.io/test/github/evanharmon1/harmon-boilerplates)

## Inspired by Other Boilerplate Repos

- <https://github.com/ChristianLempa/boilerplates>
- <https://github.com/docker/awesome-compose>
- <https://github.com/Haxxnet/Compose-Examples>
- <https://awesome-docker-compose.com/>
- <https://github.com/gruntwork-io/boilerplate>
- <https://github.com/EinGuterWaran/awesome-opensource-boilerplates?utm_source=chatgpt.com>
- <https://github.com/melvin0008/awesome-projects-boilerplates?utm_source=chatgpt.com>
- <https://boilerplatelist.com/collection/?utm_source=chatgpt.com>

## Setup & Installation

Start with looking at <https://github.com/ChristianLempa/boilerplates> repo for an existing boilerplate there. There is a cli tool to use boilerplates from that repo and you can integrate other repos.

### Requirements

- Homebrew
- Python
- [Taskfile](https://taskfile.dev/)

### Bootstrap

Install required software to run other project installers and task runners
`task bootstrap`

### Install

Install required dependencies
`task install`

## Usage

TODO: project usage

### Task Runner

[Taskfile.yaml](./Taskfile.yml)

### Testing

#### Validate

`task validate`

#### Security

`task security`

#### Linting, Formatting, Conventions, Style Guidelines, etc

- .pre-commit-config.yaml
- .shellcheckrc
- .ansible-lint-ignore

### Building, Deploying, & CI/CD

## Todo File

[todo.md](./todo.md)
