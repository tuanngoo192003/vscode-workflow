# 🐳 Custom Dev Containers

This repository provides preconfigured **Dev Containers** (`.devcontainer`) that you can use in [VS Code Remote - Containers](https://code.visualstudio.com/docs/remote/containers).
These are my personal development workflows but are also available for anyone who wants to try them out.

---

## 📂 Available Dev Containers

* Currently provided for 2 language i'm mainly working on: Java and Go
* Each language will have `.devcontainer/` directories seperated by based container source and based OS.
* Inside `.devcontainer/` contains configuration you can copy into your own projects.

---

## 📦 Inside .devcontainer

Each `.devcontainer` includes:

* A base image (e.g., [`eclipse-temurin`](https://hub.docker.com/_/eclipse-temurin) or [`mcr.microsoft.com/devcontainers`](https://mcr.microsoft.com/) images).
* Preinstalled development tools (like Git, Curl, Make, Vim, etc.).
* A ready-to-use environment for certain language development (Java 8, 11, 17, 21 | Go 1.24.0, 1.25.0,...).
* Configurations that make it easy to spin up consistent dev environments across machines.

---

## 🚀 How to Use

### VS Code Dev Containers

1. Clone this repository:

   ```bash
   git clone https://github.com/tuanngoo192003/vscode-workflow.git
   cd vscode-workflow
   ```
2. Open the folder in VS Code.
3. When prompted, “**Reopen in Container**”, click it.
   VS Code will build and start the container environment.

---

## 🤝 Contributing

This started as my personal setup, but MRs are welcome if you have improvements (e.g., adding more languages, better defaults, or new tools).

---

## 📜 License

No license :D 
Free to use, modify, and share.


