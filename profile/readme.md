# Welcome to the Grand Stew!!

[<img src="https://i.pinimg.com/originals/00/66/5c/00665c0525ca80a8a8dfb5777c9c5a04.jpg">](https://i.pinimg.com/originals/00/66/5c/00665c0525ca80a8a8dfb5777c9c5a04.jpg)
# Stew
## Install

### Brew Installlation
- Install using brew
``` 
brew tap The-Grand-Stew/stew
brew install stew
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

## Contacts:
- Vedashree Patil   vedapatil@deloitte.nl
- Aashrit Shankar   aasshankar@deloitte.nl
- Arun Kutty        arkutty@deloitte.nl

# Contribution Guide:
## Requirements:
- Linux/MacOS
- Go >= v1.17
- Preferred Code editor: VSCode

## Coding standards with Go:
### Folders
#### pkg
- All public code goes inside this package
- The code/packages written under pkg can be used universally (that means by any other application across the Go world)
- One package inside pkg cannot import from another package under pkg
- Eg of packages to put under pkg can be "logging",common functions calling external web apis, database connection scripts
#### internal
- All code internal to the application i.e business specific logic goes inside internal
- The code within this will never be public.

#### cmd
## Template Specifications


