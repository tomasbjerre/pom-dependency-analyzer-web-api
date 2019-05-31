# Pom Dependency Analyzer Web API
[![Build Status](https://travis-ci.org/tomasbjerre/pom-dependency-analyzer-web-api.svg?branch=master)](https://travis-ci.org/tomasbjerre/pom-dependency-analyzer-web-api)
[![NPM](https://img.shields.io/npm/v/pom-dependency-analyzer-web-api.svg?style=flat-square) ](https://www.npmjs.com/package/pom-dependency-analyzer-web-api)

Uses output of [Pom Dependency Analyzer](https://github.com/tomasbjerre/pom-dependency-analyzer) to create an API implementation. The implementation is completely static and can be served from [Github pages](https://pages.github.com/), [Gitlab pages](https://docs.gitlab.com/ce/user/project/pages/) or by cloning the repo and running on `localhost`.

API documented in [swagger.yml](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/tomasbjerre/pom-dependency-analyzer-web-api/master/swagger.yml).

Example:

```shell
npx pom-dependency-analyzer-web-api -sf metadata/folder -af gh-pages/api
```

Or with java:

```shell
java -jar pom-dependency-analyzer-web-api-*.jar -sf metadata/folder -af gh-pages/api
```

# Usage

```shell
-af, --api-folder <string>                 If supplied, it will dump all API-
                                           responses here.
                                           <string>: any string
                                           Default: null
-h, --help <argument-to-print-help-for>    <argument-to-print-help-for>: an argument to print help for
                                           Default: If no specific parameter is given the whole usage text is given
-ksr, --keep-server-running <boolean>      Keeps the server running.
                                           <boolean>: true or false
                                           Default: false
-md, --metadata <string>                   These key/values will be stored 
                                           together with the artifact. Can be used to 
                                           record things like artifacts git repo or 
                                           artifacts Jenkins job URL. [Supports Multiple occurrences]
                                           <string>: any string
                                           Default: Empty list
-sf, --storage-folder <string>             This is where it will look for 
                                           output of Pom Dependency Analyzer.
                                           <string>: any string
                                           Default: <user home>/.m2/repository
```
