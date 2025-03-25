# tooldemopresentationslides-DP8801

# BugZoo: A Decentralised Platform for Historical Software Bugs

BugZoo is a platform designed for distributing, reproducing, and interacting with historical software bugs. It supports software engineering researchers and developers working on testing, analysis, and automated program repair (APR) tools by leveraging Docker containers for isolated, reproducible experimentation.

---

## Installation

### Prerequisites

- **Python ≥ 3.5**
- **Docker** (Ensure Docker is installed and your user has necessary permissions)

### Installing BugZoo

```bash
pip3 install bugzoo
```

### Verify Installation

```bash
bugzoo --version
```

---

## Command-Line Interface (CLI)

### Source Commands

**Add a Source**

```bash
bugzoo source add manybugs https://github.com/squaresLab/ManyBugs
```

**List Registered Sources**

```bash
bugzoo source list
```

**Remove a Source**

```bash
bugzoo source remove https://github.com/squaresLab/ArduBugs
```

**Update Sources**

```bash
bugzoo source update
```

### Bug Commands

**List Bugs**

```bash
bugzoo bug list
```

**Build a Bug Docker Image**

```bash
bugzoo bug build manybugs:libtiff:2005-12-14-6746b87-0d3d51d
```

**Download a Bug Image**

```bash
bugzoo bug download manybugs:python:69223-69224
```

**Uninstall a Bug**

```bash
bugzoo bug uninstall manybugs:python:69223-69224
```

**Validate a Bug**

```bash
bugzoo bug validate manybugs:python:69223-69224
```

### Container Commands

**Launch a Container**

```bash
bugzoo container launch manybugs:python:69223-69224
```

**Launch with a Custom Name**

```bash
bugzoo container launch --name pybug manybugs:python:69223-69224
```

**Launch with Volume Mounting**

```bash
bugzoo container launch -v ${PWD}/db:/opt/db manybugs:python:69223-69224
```

**Launch with Tools Mounted**

```bash
bugzoo container launch --with genprog manybugs:python:69223-69224
```

### Tool Commands

**List Tools**

```bash
bugzoo tool list
```

**Build a Tool Docker Image**

```bash
bugzoo tool build genprog
```

**Download a Tool Image**

```bash
bugzoo tool download genprog
```

**Uninstall a Tool**

```bash
bugzoo tool uninstall genprog
```

**Upload a Tool (For Maintainers)**

```bash
bugzoo tool upload genprog
```

---

## Conclusion

This README file covers essential BugZoo installation steps and demonstrates how to effectively use various BugZoo commands. For more detailed documentation, refer to the official [BugZoo GitHub repository](https://github.com/squaresLab/BugZoo).

---
### Video of the tool execution

[Link](https://drive.google.com/file/d/1P87BFtugPi4U9YW1sCEfET5qPcTc6S_z/view?usp=sharing)
