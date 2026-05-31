# End-to-End Jenkins CI/CD Pipeline

## What is End-to-End CI/CD?

End-to-End CI/CD automates the complete software delivery process.

Typical workflow:

```text
GitHub → Jenkins → Maven → Docker → Deployment
```

Jenkins coordinates the pipeline and automates build, test, and deployment activities. :contentReference[oaicite:1]{index=1}

---

# Tools Used

This project uses:

- Jenkins
- GitHub
- Maven
- Docker
- Java / Spring Boot

---

# CI/CD Workflow

Pipeline flow:

```text
Developer Push Code
        ↓
GitHub Repository
        ↓
Jenkins Pipeline
        ↓
Maven Build
        ↓
Docker Build
        ↓
Deployment
```

---

# Jenkinsfile

Pipeline configuration is stored inside:

```text
Jenkinsfile
```

Example:

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

Adapted from lecture practical. :contentReference[oaicite:2]{index=2}

---

# Dockerfile

Example Dockerfile:

```dockerfile
FROM openjdk:17

COPY target/*.jar app.jar

ENTRYPOINT ["java","-jar","/app.jar"]
```

---

# Maven Build

Common command:

```bash
mvn clean package
```

Purpose:

- compile project
- run tests
- generate JAR artifact

---

# Jenkins Pipeline Setup

Steps:

1. Create GitHub Repository
2. Configure Jenkins Job
3. Select **Pipeline from SCM**
4. Configure Git Repository URL
5. Set Script Path → `Jenkinsfile`
6. Run Build

:contentReference[oaicite:3]{index=3}

---

# Advantages

- Fully automated pipeline
- Faster builds
- Repeatable deployments
- Version-controlled workflows
- DevOps automation

---

# Important Viva Questions

## What is End-to-End CI/CD?

Automated software build, testing, and deployment workflow.

---

## Which file stores Jenkins pipeline?

```text
Jenkinsfile
```

---

## Which build tool is used?

Maven.

---

## Which container tool is used?

Docker.

---

## Why use Pipeline from SCM?

To load pipeline code directly from Git repository.

---

# Conclusion

Jenkins enables complete CI/CD automation by integrating GitHub, Maven, Docker, and pipeline workflows.