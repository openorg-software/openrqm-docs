# OpenRQM System Architecture

[![Build Status](https://dev.azure.com/OpenRQM/OpenRQM/_apis/build/status/openrqm.openrqm-docs?branchName=master)](https://dev.azure.com/OpenRQM/OpenRQM/_build/latest?definitionId=5&branchName=master)

This repository contains the architecture of the OpenRQM (**open** source **r**e**q**uirement **m**anagement) System.

## Swagger/OpenAPI Code Generation

Download the OpenAPI generator: https://github.com/OpenAPITools/openapi-generator
E.g.: http://central.maven.org/maven2/org/openapitools/openapi-generator-cli/4.2.0/openapi-generator-cli-4.2.0.jar

### Generate for angular

- Windows: E.g.: `java -jar .\openapi-generator-cli-4.2.0.jar generate -i .\api\swagger.json -g typescript-angular -o .\generated\ -c .\api\angular-config.json`
- Linux: See azure-pipelines.yml

Prepare for publish in generator output directory:
- `npm install`
- `npm run build`

Publish in generator output directory:
- `npm publish dist`
