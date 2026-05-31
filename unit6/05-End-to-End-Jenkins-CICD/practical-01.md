# Practical 05 — End-to-End Jenkins CI/CD Pipeline using Docker

## Aim

To set up Jenkins using Docker container and create an end-to-end Continuous Integration (CI) pipeline for building a Java Maven project.

---

## Problem Statement

Create a Jenkins CI/CD pipeline that automatically:

- Connects with GitHub repository
- Clones project source code
- Uses Maven and JDK tools
- Builds Java project using Maven
- Generates successful build output through Jenkins Pipeline.

---

## Solution

### Step 1 — Pull Jenkins Docker Image

Downloaded Jenkins official Docker image.

Command used:

```bash
docker pull jenkins/jenkins:lts
```

Output:

```text
Status: Downloaded newer image for jenkins/jenkins:lts
```

---

### Step 2 — Start Jenkins Container

Started Jenkins inside Docker container.

Command used:

```bash
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts
```

Container started successfully.

---

### Step 3 — Open Jenkins Dashboard

Opened browser:

```text
http://localhost:8080
```

Unlocked Jenkins using administrator password.

Installed recommended plugins.

---

### Step 4 — Configure Global Tools

Navigation:

```text
Manage Jenkins
→ Tools
```

Configured JDK and Maven.

#### JDK Configuration

```text
Name: JDK17
Install Automatically: Enabled
```

#### Maven Configuration

```text
Name: Maven
Version: 3.9.16
Install Automatically: Enabled
```

---

### Step 5 — Create Jenkins Pipeline Project

Created new Jenkins job.

Navigation:

```text
New Item
→ Pipeline
```

Pipeline Name:

```text
java-maven-pipeline
```

---

### Step 6 — Configure Pipeline Script

Created Declarative Jenkins Pipeline.

Pipeline Script:

```groovy
pipeline {

    agent any

    tools {

        maven 'Maven'
        jdk 'JDK17'
    }

    stages {

        stage('Checkout') {

            steps {

                git branch: 'main',
                    url: 'https://github.com/AsthaMaurya05/devops.git'
            }
        }

        stage('Build') {

            steps {

                dir('unit5/06-Java-Maven-CI/java-ci-demo') {

                    sh 'mvn clean package'
                }

            }
        }

    }

}
```

---

### Step 7 — Execute Build Pipeline

Clicked:

```text
Build Now
```

Jenkins executed:

- Repository checkout
- Maven installation
- JDK setup
- Dependency download
- Java build process
- JAR package generation

---

### Step 8 — Verify Console Output

Console output showed successful build.

Output:

```text
[INFO] BUILD SUCCESS
Finished: SUCCESS
```

Pipeline completed successfully.

---

## Screenshots

### Jenkins Image Pull

```text
screenshots/jenkins-pull.png
```

![Jenkins Pull](screenshots/jenkins-pull.png)

---

### Docker Container Running

```text
screenshots/docker-container-running.png
```

![Docker Container](screenshots/docker-container-running.png)

---

### Jenkins Dashboard

```text
screenshots/jenkins-dashboard.png
```

![Jenkins Dashboard](screenshots/jenkins-dashboard.png)

---

### JDK and Maven Tool Configuration

```text
screenshots/tool-configuration.png
```

![Tool Configuration](screenshots/tool-configuration.png)

---

### Pipeline Script Configuration

```text
screenshots/pipeline-script.png
```

![Pipeline Script](screenshots/pipeline-script.png)

---

### Initial Failed Build (Branch Configuration Issue)

```text
screenshots/build-failure.png
```

![Build Failure](screenshots/build-failure.png)

---

### Updated Pipeline Script Fix

```text
screenshots/pipeline-fix.png
```

![Pipeline Fix](screenshots/pipeline-fix.png)

---

### Successful Build Console Output

```text
screenshots/build-success.png
```

![Build Success](screenshots/build-success.png)

---

### Final Jenkins Dashboard

```text
screenshots/final-dashboard.png
```

![Final Dashboard](screenshots/final-dashboard.png)

---

## Result

Successfully configured Jenkins using Docker container and implemented an end-to-end CI pipeline for a Java Maven project. Jenkins successfully cloned the GitHub repository, executed Maven build commands, and generated successful build output.
