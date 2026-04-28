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

## Integration with sudo

If you are a non-root user and run the `vm` command via `sudo`, apply the following settings to ensure that completion works properly.
There might be better ways to do this, but this approach works well.

1. Configure sudo to allow running the `vm` command without a password
2. Add the following shell-function in your `.zshrc`

```sh
vm()
{
    \sudo vm $@
}
```
