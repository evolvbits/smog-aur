<p align="center">
  <img style="border-radius: 5px;" src="https://raw.githubusercontent.com/evolvbits/smog/refs/heads/main/.github/logo/compact/smog-git.svg" alt="smog" width="180"/>
</p>

<h1 align="center">Turn data into unreadable noise.</h1>

AUR packaging for **Smog**

---

## 🔧 Maintainer workflow (AUR)

### Build package with script `init.sh`

```sh
sh init.sh build
```

### Install package local with script `init.sh` (test)

```sh
sh init.sh install
```

> Note: Always test with `sh init.sh install` before pushing in AUR.

### Clean all build with script `init.sh`

```sh
sh init.sh clean
```

---

## 🚀 Initial publish to AUR

```sh
sh init.sh publish
```

---

## 🔁 Updating package when a new GitHub tag is released

Example: new version `0.3.2`

1. Update version in `init.sh`:

```sh
# edit init.sh
PKGVER=0.3.2
```

2. Recalculate checksums:

```sh
sh init.sh check
```

3. Rebuild:

```sh
sh init.sh build
```

4. Commit and push:

```sh
sh init.sh publish
```

Done.

---

## 📂 Templates in this repository

* `PKGBUILD.template` — AUR build recipe
* `smog.install.template` — post-install message

---

## 🧠 Notes

* This repository does **not** contain the source code.
* The PKGBUILD downloads the source directly from GitHub releases.
* Always test with `sh init.sh install` before pushing.

---

## ✅ Maintainer best practices

Never edit `.SRCINFO` manually.
Never update `sha256sums` by hand.
Always use:

```sh
sh init.sh check
```

##  Official page

https://evolvbits.github.io/products/smog/


---

© [Evolvbits](https://evolvbits.github.io) - All rights reserved.