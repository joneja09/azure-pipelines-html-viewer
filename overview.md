# Azure Devops Portal HTML Report

## About

This Azure DevOps extension provides task for Publishing HTML Reports into built into Azure Storage.

Reports can be viewed as a tab in Build and Release result page. Each Tab contains embeded reports as well as direct download links.

For more info please refer to documentation page on [GitHub](https://github.com/joneja09/azure-pipelines-html-viewer)

## Configuration

In order to use this extension first add `Upload Portal HTML Report` task to your pipeline. In your Portal HTML Report execution task add `html` reporter that will generate `HTML` reports.

This tasks takes two parameters - required `reportDirs` which is a ',' separated list of paths to the location(s) where the HTML reports are stored and also optional `tabName` which is the name of the tab displayed within Azure DevOps report.

```YAML
steps:
- task: UploadPortalHtmlReport@1
  displayName: 'Upload Portal Html Report'
  inputs:
    cwd: '$(System.DefaultWorkingDirectory)'
    tabName: 'Portal Test'
```
