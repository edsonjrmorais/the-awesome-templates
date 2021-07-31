# The Awesome CI Templates

## Usage

The pipeline of each service will make reference to the templates that are versioned on this repository. You need to reference this repository as a resource and then on your stages reference the corresponding building block (with the required parameters).

```yaml
resources:
  repositories:
    - repository: edsonjrmorais/the-awesome-templates
      type: github
      ref: refs/heads/main
      name: AwesomeCompanyTemplates
      endpoint: ServiceConnectToGitHub

stages:    
- template: build.yml@edsonjrmorais/the-awesome-templates
  parameters:
    param1: param-value
```
