# Jenkins Pipelines

## What is a Jenkins Pipeline?

A Jenkins Pipeline is a set of automated steps that Jenkins follows to:

- build application
- run tests
- deploy software

Think of it as a **scripted flowchart for DevOps automation**. :contentReference[oaicite:0]{index=0}

---

# Why Use Pipelines?

Pipelines help:

- automate CI/CD workflows
- create repeatable builds
- define build process as code
- support complex automation

Advantages:

- version controlled workflows
- reproducible builds
- easier collaboration
- automation of entire software lifecycle

---

# Pipeline as Code

Jenkins allows defining workflows using code.

This concept is called:

```text
Pipeline as Code
```

Pipeline configuration is stored in:

```text
Jenkinsfile
```

---

# Example Pipeline Flow

Typical workflow:

```text
Code
 ↓
Build
 ↓
Test
 ↓
Deploy
```

---

# Types of Pipelines

Jenkins supports two pipeline styles.

---

## 1. Declarative Pipeline

Recommended for beginners.

Characteristics:

- easier syntax
- structured format
- easier maintenance

Example:

```groovy
pipeline {

    agent any

    stages {

        stage('Build') {

            steps {

                echo 'Building Application'
            }
        }
    }
}
```

:contentReference[oaicite:1]{index=1}

---

## 2. Scripted Pipeline

More flexible.

Uses **Groovy scripting**.

Suitable for advanced workflows.

Example:

```groovy
node {

    stage('Build') {

        echo 'Building Application'
    }
}
```

---

# Jenkinsfile

A Jenkinsfile stores pipeline definition.

Usually kept inside project repository.

Example from lecture practical:

```groovy
pipeline {

    agent any

    tools {

        maven 'Maven'
    }

    stages {

        stage('Build') {

            steps {

                bat 'mvn clean package'
            }
        }
    }
}
```

Adapted from PPT practical example. :contentReference[oaicite:2]{index=2}

---

# Pipeline Stages

Common stages:

| Stage | Purpose |
|-------|-------|
| Build | Compile project |
| Test | Execute tests |
| Package | Generate artifact |
| Deploy | Release application |

---

# Important Viva Questions

## What is a Jenkins Pipeline?

Automated CI/CD workflow definition.

---

## What is Pipeline as Code?

Defining pipeline using code stored in repository.

---

## What file stores Jenkins Pipeline?

```text
Jenkinsfile
```

---

## Difference between Declarative and Scripted Pipeline?

Declarative → simple, structured.

Scripted → flexible, Groovy-based.

---

## Why use Jenkins Pipelines?

To automate software build, testing, and deployment.

---

# Conclusion

Jenkins Pipelines automate CI/CD workflows and support version-controlled build automation using Jenkinsfile.