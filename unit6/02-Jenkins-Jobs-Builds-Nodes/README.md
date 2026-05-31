# Jenkins Jobs, Builds, Nodes and Projects

## Jenkins Core Concepts

Jenkins uses several important concepts to automate workflows:

- Jobs / Projects
- Builds
- Nodes
- Pipelines
- Plugins

These are the core building blocks of Jenkins automation. :contentReference[oaicite:0]{index=0}

---

# 1. Job / Project

A **Job** (or Project) is a task executed by Jenkins.

Think of a job as:

```text
Tell Jenkins what to do and when to do it.
```

Examples:

- build Java application
- run tests
- deploy application
- execute scripts

---

## Creating a Job

Steps:

1. Open Jenkins Dashboard
2. Click **New Item**
3. Enter project name
4. Select **Freestyle Project**
5. Configure build settings
6. Click **Save**

:contentReference[oaicite:1]{index=1}

---

# 2. Build

A **Build** is a single execution of a Jenkins job.

Each build has:

- Build Number
- Build Status
- Console Output
- Execution Logs

Common statuses:

| Status | Meaning |
|--------|--------|
| Success | Build completed successfully |
| Failed | Build encountered error |
| Running | Build currently executing |

---

# 3. Node

A **Node** is a machine where Jenkins executes jobs.

Types:

## Master / Controller Node

Controls Jenkins system.

Responsibilities:

- manage jobs
- schedule builds
- control agents

---

## Agent / Slave Node

Executes assigned jobs.

Used for:

- distributed builds
- workload sharing
- parallel execution

:contentReference[oaicite:2]{index=2}

---

# 4. Pipeline

A **Pipeline** defines automated workflow steps.

Example:

```text
Code → Build → Test → Deploy
```

Pipelines can be:

- Declarative Pipeline
- Scripted Pipeline

---

# 5. Plugins

Plugins extend Jenkins functionality.

Examples:

- Git Plugin
- Docker Plugin
- Maven Integration Plugin
- Pipeline Plugin

---

# Why These Concepts Matter

These concepts help Jenkins support:

- CI automation
- CD pipelines
- distributed builds
- tool integrations

---

# Important Viva Questions

## What is a Jenkins Job?

Task executed by Jenkins.

---

## What is a Build?

Single execution of a Jenkins job.

---

## What is a Node?

Machine used by Jenkins to run jobs.

---

## Difference between Master and Agent Node?

Master → manages Jenkins.

Agent → executes jobs.

---

## What is a Pipeline?

Automated sequence of CI/CD stages.

---

# Conclusion

Jobs, builds, nodes, pipelines, and plugins form the foundation of Jenkins automation workflows.

