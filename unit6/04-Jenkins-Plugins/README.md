# Jenkins Plugins

## What are Jenkins Plugins?

Plugins are add-ons that extend Jenkins functionality.

They allow Jenkins to integrate with external tools and services.

Without plugins, Jenkins is only a basic automation server. :contentReference[oaicite:0]{index=0}

---

# Why Are Plugins Important?

Plugins help Jenkins:

- connect to source code repositories
- support build tools
- send notifications
- use containers
- create CI/CD pipelines

Plugins make Jenkins highly customizable.

---

# Common Jenkins Plugins

## Git Plugin

Purpose:

Integrates Jenkins with Git repositories.

Supports:

- GitHub
- GitLab
- Bitbucket

---

## Maven Integration Plugin

Purpose:

Allows Jenkins to build Maven projects.

Example:

```text
mvn clean package
```

---

## Docker Plugin

Purpose:

Integrates Jenkins with Docker.

Supports:

- Docker builds
- Docker containers
- Docker pipelines

---

## Pipeline Plugin

Purpose:

Supports Jenkins Pipelines.

Enables:

- Pipeline as Code
- Jenkinsfile execution
- CI/CD automation

---

## HTML Publisher Plugin

Purpose:

Publishes HTML reports generated during builds.

---

## SSH Agent Plugin

Purpose:

Provides SSH authentication during builds and deployments.

---

# Installing Plugins

Steps:

1. Open Jenkins Dashboard
2. Click **Manage Jenkins**
3. Select **Manage Plugins**
4. Search plugin
5. Click **Install without restart**

:contentReference[oaicite:1]{index=1}

---

# Plugins Used in CI/CD

Common plugins used with Jenkins:

| Plugin | Purpose |
|--------|--------|
| Git Plugin | Source control integration |
| Docker Plugin | Container integration |
| Maven Plugin | Java builds |
| Pipeline Plugin | Workflow automation |
| HTML Publisher | Report publishing |

---

# Advantages of Plugins

- Extend Jenkins capabilities
- Tool integrations
- Flexible automation
- Custom workflows
- Better CI/CD support

---

# Important Viva Questions

## What is a Jenkins Plugin?

Add-on used to extend Jenkins functionality.

---

## Why are plugins important?

They provide integrations and extra features.

---

## Which plugin integrates Git with Jenkins?

Git Plugin.

---

## Which plugin supports Docker workflows?

Docker Plugin.

---

## Which plugin supports Maven builds?

Maven Integration Plugin.

---

# Conclusion

Jenkins plugins expand automation capabilities and enable integration with development, build, testing, and deployment tools.
