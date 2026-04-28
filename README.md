<p align="center">
  <img style="border-radius: 5px;" src="https://raw.githubusercontent.com/evolvbits/smog/refs/heads/main/.github/logo/compact/smog-git.svg" alt="smog" width="180"/>
</p>

<h1 align="center">Turn data into unreadable noise.</h1>

AUR packaging for **Smog**

---

## 🔧 Maintainer workflow (AUR)

### Build package with script `run`

```sh
./run build
```

### Install package local with script `run` (test)

```sh
./run install
```

> Note: Always test with `./run install` before pushing in AUR.

### Clean all build with script `run`

```sh
./run clean
```

---

## 🚀 Initial publish to AUR

```sh
./run publish
```

---

## 🔁 Updating package when a new GitHub tag is released

Example: new version `0.3.2`

1. Update version in `run`:

```sh
# edit run
PKGVER=0.3.2
```

2. Recalculate checksums:

```sh
./run check
```

3. Rebuild:

```sh
./run build
```

4. Commit and push:

```sh
./run publish
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
* Always test with `./run install` before pushing.

---

## ✅ Maintainer best practices

Never edit `.SRCINFO` manually.
Never update `sha256sums` by hand.
Always use:

```sh
./run check
```

##  Official page

https://evolvbits.github.io/products/smog/


---

© [Evolvbits](https://evolvbits.github.io) - All rights reserved.