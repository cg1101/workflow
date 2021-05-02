# Workflow

[![deploy_to_gcloud](https://github.com/cg1101/workflow/actions/workflows/deploy.yml/badge.svg)](https://github.com/cg1101/workflow/actions/workflows/deploy.yml)

This project is toy project that is designed to explores following things:

* workflow implemented with github actions
* use of environments
* dependabot
* web page hosted on github

## Configure Environments

From repo home, go to `Settings` and then `Environments`, click `New Environment` to create new environments

## Add workflow

Add file `.github/workflow/deploy.yml` to the repo. The filename can be anything you like. Then edit its content that is needed by our CI/CD pipeline.

## Add dependabot

Create file `.github/dependabot.yml` and edit its contents. This enables dependabot to periodically scan your repo for security vulnerabilities.

## Add a web page

From repo home, go to `Settings` and then `Pages`, configure source and edit your html file.

## Branching strategy

Branch / Environment mapping relationships are as follows:

Branch    | Environment
----------|------------
main      | prod
release   | uat
integrate | test
develop   | dev
\*        | poc

## Add new features

First, create a new feature branch from latest `develop` branch.

```sh
git checkout develop
git pull
git checkout -b feature/new-feat
```

Then make your change in your new feature branch. Once change is done and test, rebase it against `develop` branch.

```sh
git rebase develop
```

Then push it to github to create PR, with the destination set to `develop` branch.

Reviewers can now review the changes made in this feature branch.

## Feature apple

This feature is to be implemented in its own branch.

## Feature banana

This feature is to be implemented in its own branch.

## Feature cherry

This feature is to be implemented in its own branch.

## Feature durian

This feature is to be implemented in its own branch.

## Feature eggplant

This feature is to be implemented in its own branch.
