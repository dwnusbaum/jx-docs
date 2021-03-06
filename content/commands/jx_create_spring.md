---
date: 2018-11-30T14:32:35Z
title: "jx create spring"
slug: jx_create_spring
url: /commands/jx_create_spring/
---
## jx create spring

Create a new Spring Boot application and import the generated code into Git and Jenkins for CI/CD

### Synopsis

Creates a new Spring Boot application and then optionally setups CI/CD pipelines and GitOps promotion. 

You can see a demo of this command here: https://jenkins-x.io/demos/create_spring/

For more documentation see: https://jenkins-x.io/developing/create-spring/

```
jx create spring [flags]
```

### Examples

```
  # Create a Spring Boot application where you use the terminal to pick the values
  jx create spring
  
  # Creates a Spring Boot application passing in the required dependencies
  jx create spring -d web -d actuator
  
  # To pick the advanced options (such as what package type maven-project/gradle-project) etc then use
  jx create spring -x
  
  # To create a gradle project use:
  jx create spring --type gradle-project
```

### Options

```
  -x, --advanced                       Advanced mode can show more detailed forms for some resource kinds like springboot
  -a, --artifact string                Artifact ID to generate
  -b, --batch-mode                     In batch mode the command never prompts for user input
  -t, --boot-version string            Spring Boot version
      --branches string                The branch pattern for branches to trigger CI/CD pipelines on
      --credentials string             The Jenkins credentials name used by the job
  -d, --dep stringArray                Spring Boot dependencies
      --docker-registry-org string     The name of the docker registry organisation to use. If not specified then the Git provider organisation will be used
      --dry-run                        Performs local changes to the repo but skips the import into Jenkins X
      --external-jenkins-url string    The jenkins url that an external git provider needs to use
      --git-api-token string           The Git API token to use for creating new Git repositories
      --git-private                    Create new Git repositories as private
      --git-provider-url string        The Git server URL to create new Git repositories inside (default "https://github.com")
      --git-username string            The Git username to use for creating new Git repositories
  -g, --group string                   Group ID to generate
      --headless                       Enable headless operation if using browser automation
  -h, --help                           help for spring
      --import-commit-message string   Should we override the Jenkinsfile in the project?
      --install-dependencies           Should any required dependencies be installed automatically
  -j, --java-version string            Java version
      --jenkinsfile string             The name of the Jenkinsfile to use. If not specified then 'Jenkinsfile' will be used
  -k, --kind stringArray               Default dependency kinds to choose from (default [Core,Web,Template Engines,SQL,I/O,Ops,Spring Cloud GCP,Azure,Cloud Contract,Cloud AWS,Cloud Messaging,Cloud Tracing])
  -l, --language string                Language to generate
      --list-packs                     list available draft packs
      --log-level string               Logging level. Possible values - panic, fatal, error, warning, info, debug. (default "info")
      --name string                    Specify the Git repository name to import the project into (if it is not already in one)
      --no-brew                        Disables the use of brew on macOS to install or upgrade command line dependencies
      --no-draft                       Disable Draft from trying to default a Dockerfile and Helm Chart
      --no-import                      Disable import after the creation
      --no-jenkinsfile                 Disable defaulting a Jenkinsfile if its missing
      --org string                     Specify the Git provider organisation to import the project into (if it is not already in one)
  -o, --output-dir string              Directory to output the project to. Defaults to the current directory
      --pack string                    The name of the pack to use
  -p, --packaging string               Packaging
      --pull-secrets string            The pull secrets the service account created should have (useful when deploying to your own private registry): provide multiple pull secrets by providing them in a singular block of quotes e.g. --pull-secrets "foo, bar, baz"
      --skip-auth-secrets-merge        Skips merging a local git auth yaml file with any pipeline secrets that are found
      --type string                    Project Type (such as maven-project or gradle-project)
      --verbose                        Enable verbose logging
```

### SEE ALSO

* [jx create](/commands/jx_create/)	 - Create a new resource

###### Auto generated by spf13/cobra on 30-Nov-2018
