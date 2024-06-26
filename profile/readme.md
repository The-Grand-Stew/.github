# Welcome to the Grand Stew!!

# Stew
## Install

### Brew Installlation
- Install using brew
``` 
brew tap The-Grand-Stew/stew
brew install stew
```
### Local Installation
```go build -o stew cmd/main.go
./stew [OPTIONS]
or
go run cmd/main.go [OPTIONS]
```

## Usage
- Export your access github token  
`export HOMEBREW_GITHUB_ACCESS_TOKEN="your-token"`
- Run `stew --help` for all command options
- Run a command and follow the steps
- To deploy on AWS, make sure the credentials are exported as env variables (Stew checks for only env vars now, profiles and loading credentials is in development)
```export AWS_ACCESS_KEY_ID=""
    export AWS_SECRET_ACCESS_KEY=""
```
- To get an CLI "app" tour:
`stew play`

## Supported Languages and Frameworks:
### Go
- Fiber
### Node
- Express
### Python
- FastAPI (coming soon)

## Support Cloud Architectures:
### AWS
- ECS Fargate
### GCP
- Cloudrun (Coming soon)




# Contribution Guide:
## Requirements:
- Linux/MacOS
- Go >= v1.17
- Preferred Code editor: VSCode

## Coding standards with Go:
### Generic Folder structure
#### pkg
- All public code goes inside this package
- The code/packages written under pkg can be used universally (that means by any other application across the Go world)
- One package inside pkg cannot import from another package under pkg
- Eg of packages to put under pkg can be "logging",common functions calling external web apis, database connection scripts
#### internal
- All code internal to the application i.e business specific logic goes inside internal
- The code within this will never be public.

#### cmd
- All your main entrypoint (main.go) go in here
### Reference Links
https://gochronicles.com/writing-go-code-like-a-pro/

https://gochronicles.com/dependency-management-in-go/

### Stew Source Code Breakdown
#### pkg/templates/*
Go templates for different languages and frameworks.
#### pkg/commands/*
Command bash commands that need run when setting up services. Eg `go mod init` needs to run when setting up go services
#### pkg/configs/
Handling stew config file **.stew** thats created when a service is setup
#### cmd/
Contains all specific code for setting up services in a language and framework
#### cmd/stew
Main commands for stew. Where each ".go" file is a command in stew

### Writing Go Text Templates
Refer:
https://blog.gopheracademy.com/advent-2017/using-go-templates/
