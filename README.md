## Void Linux template file for xbps-src

Instructions for building `hypr` on void linux using `xbps-src`:

1. Setup the `void-packages` repo:

```sh
❯ git clone --depth=1 https://github.com/void-linux/void-packages
❯ cd void-packages
❯ ./xbps-src binary-bootstrap
❯ echo XBPS_ALLOW_RESTRICTED=yes >> etc/conf
```

2. Download the template repo and copy into `srcpkgs`:

```sh
❯ git clone https://github.com/Flammable-Duck/hypr-template
❯ mv hypr-template ./srcpkgs/hypr
```

3. Build & install the package:

```sh
❯ ./xbps-src pkg hypr
❯ sudo xbps-install --repository=hostdir/binpkgs hypr
```

**Note #1:** if you have `xtools` installed you can install the package by running `xi -f hypr` (instead of using `xbps-install`).

---
This is my first void package, so please feel free to let me know if there are problems with it.

Special thanks to [@ibhagwan](https://github.com/ibhagwan), who I shamelessly stole this readme from
