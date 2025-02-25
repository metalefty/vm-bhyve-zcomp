# vm-bhyve-zcomp
Zsh completion for [vm-bhyve](https://github.com/churchers/vm-bhyve).

## Usage

Install `_vm` to `/usr/local/share/zsh/site-functions` or a whatever way you like.

## Usage (development)

Clone the repository first.

```sh
git clone https://github.com/metalefty/vm-bhyve-zcomp.git
```

Your `.zshrc` must already have like below if you're already using other completions.

```sh
autoload -Uz compinit && compinit
```

Add the path of vm-bhyve-zcomp to fpath.
```diff
+fpath=(~/path/to/vm-bhyve-zcomp $fpath)
autoload -Uz compinit && compinit
```

Run `exec zsh` to reload.
