# [Status page](https://status.nextpost.tech) for [Nextpost.tech](https://nextpost.tech)

<!--start: description-->

This repository contains the uptime monitor and status page for [Nextpost.tech](https://nextpost.tech).

<!--end: description-->

[![Uptime CI](https://github.com/nextpost-tech/status/workflows/Uptime%20CI/badge.svg)](https://github.com/upptime/upptime/actions?query=workflow%3A%22Uptime+CI%22)
[![Response Time CI](https://github.com/nextpost-tech/status/workflows/Response%20Time%20CI/badge.svg)](https://github.com/upptime/upptime/actions?query=workflow%3A%22Response+Time+CI%22)
[![Graphs CI](https://github.com/nextpost-tech/status/workflows/Graphs%20CI/badge.svg)](https://github.com/upptime/upptime/actions?query=workflow%3A%22Graphs+CI%22)
[![Static Site CI](https://github.com/nextpost-tech/status/workflows/Static%20Site%20CI/badge.svg)](https://github.com/upptime/upptime/actions?query=workflow%3A%22Static+Site+CI%22)
[![Summary CI](https://github.com/nextpost-tech/status/workflows/Summary%20CI/badge.svg)](https://github.com/upptime/upptime/actions?query=workflow%3A%22Summary+CI%22)

## [Live Status](https://status.nextpost.tech): <!--live status-->

<!--start: status pages-->
<!--end: status pages-->

<!--start: docs-->

## How it works

GitHub Actions is used as an uptime monitor:
- Every 5 minutes, a workflow visits our server to make sure it's up
- Response time is recorded every 6 hours and committed to git
- Graphs of response time are generated every day

GitHub Issues are used for incident reports:
- An issue is opened if an endpoint is down
- People from our team are assigned to the issue
- Incidents reports are posted as issue comments
- Issues are locked so non-members cannot comment on them
- Issues are closed automatically when our sites comes back up
- Telegram notifications are sent on updates

GitHub Pages are used for the status website:
- A simple, beautiful, and accessible PWA is generated
- Built with Svelte and Sapper
- Fetches data from this repository using the GitHub API

## Issues as incidents

When the GitHub Actions workflow detects that one of our URLs is down, it automatically opens a GitHub issue . We add incident reports to this issue by adding comments. When our site comes back up, the issue will be closed automatically as well.

## Commits for response time

Four times per day, another workflow runs and records the response time of our servers. This data is commited to GitHub, so it's available in the commit history of each file. Then, the GitHub API is used to graph the response time history of each endpoint and to track when a site went down.

Build on [Upptime](https://upptime.js.org).




