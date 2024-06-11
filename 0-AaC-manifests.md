# Architecture-as-Code manifests

## Introduction

AaC manifests describe FlexStack components and reside as JSON(c)/YAML in your Git repositories.
They are used to define the configuration of your components such as resource limits, environment-specific 
configurations, build arguments, environment variables, and more.

## Example manifest

```jsonc
// flexstack.jsonc
{
  "$schema": "https://flexstack.com/manifest",
  "type": "web-service",
  
  "name": "api",
  "cpu": 0.25,
  "source": {
    "git": {
      "branch": "staging",
    },
  },

  "environments": {
    "production": {
      "cpu": 0.5,
      "memory": 1,
      "source": {
        "git": {
          "branch": "main",
        },
      },
    },
  },
}
```

## Target date

Q3 2024