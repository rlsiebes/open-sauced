<div align="center">
  <br>
  <img alt="Open Sauced" src="https://i.ibb.co/7jPXt0Z/logo1-92f1a87f.png" width="500px">
  <h1>🍕 Open Sauced 🍕</h1>
  <strong>The path to your next Open Source contribution</strong>
</div>
<br>
<p align="center">
  <a href="https://github.com/bdougie/open-sauced/actions?query=workflow%3A%22Node+CI%22">
    <img src="https://github.com/bdougie/open-sauced/workflows/Node%20CI/badge.svg" alt="Node CI">
  </a>
  <a href="https://app.netlify.com/sites/open-sauced/deploys">
    <img src="https://api.netlify.com/api/v1/badges/76a3de8e-270c-4adf-89d5-3a3863da74e6/deploy-status" alt="Netlify Status">
  </a>
  <img src="https://badgen.net/dependabot/bdougie/open-sauced?icon=dependabot" alt="Dependabot Badge">
  <img src="https://img.shields.io/github/languages/code-size/bdougie/open-sauced" alt="GitHub code size in bytes">
  <img src="https://img.shields.io/github/commit-activity/w/bdougie/open-sauced" alt="GitHub commit activity">
  <a href="https://github.com/bdougie/open-sauced/issues">
    <img src="https://img.shields.io/github/issues/bdougie/open-sauced" alt="GitHub issues">
  </a>
</p>

# Open Sauced

This is a GraphQL starter project to help people stalk open source repositories and take notes on them. This project uses OneGraphl as an interface to the GitHub [GraphQL API](https://developer.github.com/v4/) and Netlify to deploy.

[![open-sauced-screencap](https://user-images.githubusercontent.com/5713670/82944481-27abec00-9f50-11ea-85c0-960641717f33.png)
](https://opensauced.pizza)

## Local development
```
npm install
npm start
```

## Test

```
npm test

// to clean snapshots
npm run clean
```
## Storybook
Storybook is being leverage to mock out visual React components. A version of it can be found at this [url](https://sauced-components.netlify.com/).
```
npm run storybook
```
![storybook example screenshot](https://user-images.githubusercontent.com/5713670/68147486-0cd14600-ff32-11e9-8cc0-fd91f4171b87.png)

## Authentication
Authentication is handled through [OneGraph's AuthGuardian](https://www.onegraph.com/docs/auth_guardian.html) service. 

## Database
This project uses GitHub as a database. When you login, you will be presented whena button to create a goals repository. That repository template lives at [open-sauced/goals-template](https://github.com/open-sauced/goals-template).

## Service Worker
This project uses the sw-precache to kickstart an offline cache. The
offline cache only registers in production. If service needs to be
manually removed make an **unregister** call from the registerServiceWorker.js import. 

