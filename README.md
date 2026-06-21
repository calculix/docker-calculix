# Docker Calculix

This project provides Docker Compose configuration to run CalculiX in a containerized environment.

CalculiX is an open-source program for Finite Element Analysis (FEA) of structural problems. This project builds and runs CalculiX 2.20 inside an Ubuntu 22.04 container, so you can use it without installing the toolchain on your host machine.

## 📦 Requirements

- [Docker](https://www.docker.com/)
- Docker Compose v2 (the `docker compose` command)

## ⚙️ Setup

### Create secret.txt

Create a text file named `secret.txt` in the project root containing the password
for the `ubuntu` user inside the container. The entire file content is used as the
password, so it should contain only the password itself:

```text
YourPassword!
```

> **Note:** `secret.txt` contains a credential and should not be committed to version control.

## 🚀 Usage

### Build and Start Docker Container

Run the following script to build the Docker image `docker-calculix-ubuntu` and start the container `ubuntu-calculix`:

```bash
./run-compose.sh
```

### Access the Container

Run the following script to enter the container:

```bash
./docker-in.sh
```

## 📚 Reference

- [CalculiX: A Three-Dimensional Structural Finite Element Program](https://www.dhondt.de)
- [Docker](https://www.docker.com/)

## 📄 License

This project is licensed under GPL 2.0.

Please see [LICENSE](./LICENSE) for details.
