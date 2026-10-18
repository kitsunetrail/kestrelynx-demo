# kestrelynx-demo

A demo repository for [KestreLynx](https://github.com/kitsunetrail/kestrelynx) remediation plans and experimental remediation PRs.

## Demo setup

This Compose configuration intentionally pins older images and dependencies:

- **proxy:** `nginx:1.27.0` in `compose.yml`.
- **api:** `python:3.12.3-slim`, with older Flask, Werkzeug, urllib3, and other packages pinned in `api/requirements.txt`.
- **web:** `node:22.12.0-slim`, with Express `4.18.2` and its dependencies locked in `web/package-lock.json`.

KestreLynx scans the running containers and automatically opens PRs in this repository to update Compose image tags, Dockerfile base images, and pip and npm dependencies. Maintainers decide whether to merge these PRs.

## Safety

This repository contains known vulnerabilities. Use it only in an isolated demo environment. Do not run it in production or on a public network.
