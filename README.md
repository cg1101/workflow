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
