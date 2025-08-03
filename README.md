# kafel-debian

Debian packaging files for [`kafel`](https://github.com/google/kafel), a C library and language for writing syscall filter policies using seccomp-BPF.

This repository contains only the `debian/` directory and supporting files needed to build Debian packages from the upstream `kafel` source.

## 📦 What is kafel?

Kafel is a domain-specific language and library for writing Linux seccomp-BPF rules. It simplifies the creation of secure syscall filters and is especially useful in sandboxing applications.

GitHub: [https://github.com/google/kafel](https://github.com/google/kafel)

---

## 🛠 How to Build the Package

These instructions assume a Debian-based system with packaging tools installed.

### 1. Clone This Repo

```bash
git clone https://github.com/stevecrozz/debian-kafel.git
```

### 2. Clone Upstream Source

```bash
git clone https://github.com/google/kafel.git
cd kafel
git checkout <version-tag>  # e.g., v1.0.0
```

### 3. Copy ./debian Folder to Upstream Source Folder

```bash
cp ../debian-kafel/debian .
```
