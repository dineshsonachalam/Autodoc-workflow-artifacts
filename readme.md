# Audodoc workflow artifacts:

### Artifacts
<!-- AUTO-GENERATED-CONTENT:START (artifactsTable) -->
<table class="artifactsTable"><thead><tr><th class="artifact-th">Artifact</th><th class="workflow-th">Workflow</th></tr></thead><tbody ><tr ><td class="artifact-td td_text"><a href=https://github.com/dineshsonachalam/Lucid-Dynamodb/suites/2942883115/artifacts/67433873>Pytest-report</a></td><td class="workflow-td td_text"><a href=https://github.com/dineshsonachalam/Lucid-Dynamodb/actions/runs/918921415>Integration-Test</a></td></tr></tbody></table><br><p>Auto generated by <a href="https://github.com/dineshsonachalam/Autodoc-workflow-artifacts">Autodoc-workflow-artifacts</a></p>
<!-- AUTO-GENERATED-CONTENT:END -->


https://stackoverflow.com/questions/62750603/github-actions-trigger-another-action-after-one-action-is-completed

Table headers: Artifact | Worflow

Publish it as npm package and also publish it as workflow action.

You need to a npm package CLI.

Also publish it as a github package.

https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry


## Installation

1. Clone the repository and then navigate to it.
2. Run ```npm install``` to install the dependencies.
3. Run ```npm install -g .``` to install the CLI. <br>

npm publish --access public

### Todo:
1. automate node publishing.
2. Add following workflows which should generate artifacts:
```
1. code coverage.
2. security vulnerabilities.
3. linting.
4. test cases report.
```

https://stackoverflow.com/questions/16633246/code-coverage-with-mocha
https://medium.com/@selvarajchinnasamyks/how-to-write-an-integration-test-for-node-js-application-4a2f4140665f


### To run test
```
npm test
npm i -g nyc
```
### Html report
Just use
```
nyc --reporter=html
```
instead of text. Now it will produce a report inside ./coverage/index.html.

https://istanbul.js.org/docs/tutorials/mocha/

# tests


npm i -g nodejs-health-checker

npm i -g .

npx license-checker --csv --out ./report.csv





npm install -g npm-audit-html
npm audit --json | npm-audit-html --output report.html 
