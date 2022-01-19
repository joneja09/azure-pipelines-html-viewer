# Azure Devops HTML Report Portal

## About

This Azure DevOps extension provides task for Publishing HTML Reports to view in a tab on the Pipeline run.

Reports can be viewed as a tab in Build and Release result pages.
Tab contains embeded reports as well as direct download links.

## Configuration

In order to use this extension first add `Upload Portal HTML Report` task to your pipeline. In your Portal execution task add `html` reporter that will generate `HTML` reports.

This tasks takes two parameters - required `reportDirs` which is the path(s) to the location where the HTML reports are stored and also optional `tabName` which is the name of the tab displayed within the Azure DevOps Pipeline run.

```YAML
steps:
- task: UploadPortalHtmlReport@1
  displayName: 'Upload Html Reports'
  inputs:
    reportDirs: '$(System.DefaultWorkingDirectory)'
    tabName: 'Test Reports'
```

![](./docs/postman-report-2.png)

## Example

### Report summary on build tab

![](./docs/postman-report-1.png)

## Contributors

<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
      <td align="center">
      <a href="https://github.com/joneja09">
        <img src="https://avatars.githubusercontent.com/u/33398109?v=4" width="100px;" alt=""/>
        <br />
        <b>Jeff Jones</b>
    </td>
  </tr>
</table>
<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
