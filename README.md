<h1 align="center">
  <a href="https://github.com/marketplace/actions/markdown-autodocs">
    <img src="https://i.imgur.com/ZAC4qPa.png"/>
  </a>
</h1>
<p align="center">A GitHub Action that automatically generates & updates markdown content (like your README.md) from external or remote files.</p>
<p align="center">
    <a href="https://sonarcloud.io/dashboard?id=markdown-autodocs">
        <img src="https://sonarcloud.io/api/project_badges/quality_gate?project=markdown-autodocs"/>
    </a>
</p>
<p align="center">
    <a href="https://www.codacy.com/gh/dineshsonachalam/markdown-autodocs/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=dineshsonachalam/markdown-autodocs&amp;utm_campaign=Badge_Grade">
        <img src="https://app.codacy.com/project/badge/Grade/55bdbc75c542444d86b8e900bb0f4f91"/>
    </a>
    <a href="https://snyk.io/test/github/dineshsonachalam/markdown-autodocs">
        <img src="https://snyk.io/test/github/dineshsonachalam/markdown-autodocs/badge.svg"/>
    </a>
    <a href="https://github.com/dineshsonachalam/markdown-autodocs/actions/workflows/tests.yml">
        <img src="https://github.com/dineshsonachalam/markdown-autodocs/actions/workflows/tests.yml/badge.svg"/>
    </a>
    <a href="https://github.com/dineshsonachalam/markdown-autodocs/actions/workflows/markdown-autodocs.yml">
        <img src="https://github.com/dineshsonachalam/markdown-autodocs/actions/workflows/markdown-autodocs.yml/badge.svg"/>
    </a>
    <a href="https://www.npmjs.com/package/markdown-autodocs">
      <img src="https://img.shields.io/npm/v/markdown-autodocs?color=dark%20green&label=npm%20package" alt="npm version" height="20">     
    </a>
    <a href="https://github.com/dineshsonachalam/markdown-autodocs/blob/master/LICENSE" target="_blank">
        <img src="https://badgen.net/github/license/dineshsonachalam/markdown-autodocs" alt="MIT License" height="20">
    </a>
</p>

Ask questions in the <a href ="https://github.com/dineshsonachalam/markdown-autodocs/issues">GitHub issues</a>

## Table of contents

*   [Why markdown-autodocs?](#why-markdown-autodocs)
*   [Features](#features)
*   [Examples](#examples)
    *   [CODE Block](#code-block)
    *   [JSON to HTML table](#json-to-html-table)
    *   [Github Workflow Artifacts table](#github-workflow-artifacts-table)
*   [Example Repo which uses all the markdown-autodocs feature](#example-repo-which-uses-all-the-markdown-autodocs-feature)
*   [Local usage without Github action](#local-usage-without-github-action)
*   [Usage](#usage)
    *   [Adding markdown-autodocs in your workflow](#adding-markdown-autodocs-in-your-workflow)
    *   [Extended example with all possible options available for this Action](#extended-example-with-all-possible-options-available-for-this-action)
*   [Github Workflow Artifacts](#github-workflow-artifacts)
*   [Contributing](#contributing)
*   [Used By](#-used-by)
*   [License](#license)

## Why markdown-autodocs
To make your repo more appealing and useful you need to provide example code snippets in your README.md. Manually copy and pasting each code snippet in their respective places in your README would be inefficient and time-consuming.

This problem can be solved using <b>markdown-autodocs</b> a GitHub Action that automatically generates & updates markdown content (like your README.md) from external or remote files. You need to add markers in your README.md that will tell markdown-autodocs where to insert the code snippet.

## Features
*   <b>Code block:</b> Insert code snippet in your markdown file from external or remote files.
*   <b>JSON to HTML table:</b> Insert HTML Table in your markdown file by converting JSON file contents to HTML table.
*   <b>Github Workflow Artifacts table:</b> Insert the Github workflow artifacts table in your markdown file by getting the latest artifacts for a workflow run.

## Examples

### CODE Block

Get code from an external file or URL and insert it in your markdown.

**Options:**
*   `src`: The relative path to the code to pull in, or the `URL` where the raw code lives

<a href="./docs/examples.md#get-code-from-external-file" target="_blank">
    <img src="https://i.imgur.com/NUMReeR.png"/>
</a>

<a href="./docs/examples.md#get-code-from-remote-file" target="_blank">
  <img src="https://i.imgur.com/blYRUXN.png"/>
</a>

### JSON to HTML table
Get JSON contents from an external file and convert it into an HTML table and insert's it in your markdown.

**Options:**
*   `src`: The relative path to the JSON file to pull in.

<a href="./docs/examples.md#json-to-html-table" target="_blank">
  <img src="https://i.imgur.com/5pTHIpS.png"/>
</a>

### Github Workflow Artifacts table

Get the list of the latest artifacts generated from a workflow run. Generates a workflow artifacts table consists of artifacts download and workflow URL in an HTML table and inserts it in your markdown file.

<a href="./docs/examples.md#github-workflow-artifacts-table" target="_blank">
  <img src="https://i.imgur.com/gVHiSB8.png"/>
</a>

### [Example Repo which uses all the markdown-autodocs feature](https://github.com/dineshsonachalam/repo-using-markdown-autodocs)

## Local usage without Github action

**Install markdown-autodocs CLI:**
```sh
npm i -g markdown-autodocs
```

**markdown-autodocs CLI usage:**
```sh
dineshsonachalam@macbook ~ % markdown-autodocs --help
Usage: markdown-autodocs [options]

Options:
  -o, --outputFilePath <outputFilePaths...>  Output file paths
  -c, --category <categories...>             code-block, json-to-html-table, workflow-artifact-table
  -r, --repo <type>                          Repo name
  -b, --branch <type>                        Branch name
  -a, --accessToken <type>                   Github Access token
  -h, --help                                 display help for command
```

*   Code block

```sh
markdown-autodocs -c code-block -o ./README.md 
```
*   JSON to HTML table

```sh
markdown-autodocs -c json-to-html-table -o ./README.md
```
*   Github workflow artifacts table

```sh
markdown-autodocs -c workflow-artifact-table -o ./README.md -r $REPO -b $BRANCH -a $ACCESSTOKEN
```

## Usage

### Adding markdown-autodocs in your workflow
Add the following step at the end of your job, after other steps that might add or change files.
<!-- MARKDOWN-AUTO-DOCS:START (CODE:src=./docs/latest-release.yml) -->
<!-- MARKDOWN-AUTO-DOCS:END -->

### Extended example with all possible options available for this Action
<!-- MARKDOWN-AUTO-DOCS:START (CODE:src=./docs/markdown-autodocs.yml) -->
<!-- MARKDOWN-AUTO-DOCS:END -->

## Github Workflow Artifacts
<!-- MARKDOWN-AUTO-DOCS:START (WORKFLOW_ARTIFACT_TABLE) -->
<!-- MARKDOWN-AUTO-DOCS:END -->

## Contributing

*   [Code of Conduct](CODE_OF_CONDUCT.md)
*   [Contributing Guideline](CONTRIBUTING.md)

## 🚀 Used By

*   [iro.js - 🎨 Modular color picker widget for JavaScript, with support for a bunch of color formats](https://github.com/jaames/iro.js)
*   [Fireworks.js - 🎆 A simple fireworks library](https://github.com/crashmax-dev/fireworks-js)
*   [LucidDynamodb - 🗄️ A minimalistic wrapper to AWS DynamoDB](https://github.com/dineshsonachalam/Lucid-Dynamodb)
*   [redis-cloudflare-kv - ⚡ Redis caching layer for Cloudflare KV in Golang](https://github.com/dineshsonachalam/redis-cloudflare-kv)

## License

[MIT](https://choosealicense.com/licenses/mit/) © [dineshsonachalam](https://www.github.com/dineshsonachalam)
