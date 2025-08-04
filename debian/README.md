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

### 2. Add a new version for the upstream release

```bash
dch -i
```

### 3. Import the upstream changes via uscan

```bash
gbp import-orig --pristine --uscan --upstream-tag='upstream/0_%(version)s' --upstream-branch=upstream
```

### 3. Build

```bash
gbp buildpackage --git-builder=debuild --git-debian-branch=main
```
