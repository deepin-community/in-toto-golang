## in-toto completion

Generate completion script

### Synopsis

To load completions:
Bash:
  $ source <(in-toto completion bash)
  # To load completions for each session, execute once:
  # Linux:
  $ in-toto completion bash > /etc/bash_completion.d/in-toto
  # macOS:
  $ in-toto completion bash > /usr/local/etc/bash_completion.d/in-toto
Zsh:
  # If shell completion is not already enabled in your environment,
  # you will need to enable it.  You can execute the following once:
  $ echo "autoload -U compinit; compinit" >> ~/.zshrc
  # To load completions for each session, execute once:
  $ in-toto completion zsh > "${fpath[1]}/_in-toto"
  # You will need to start a new shell for this setup to take effect.
fish:
  $ in-toto completion fish | source
  # To load completions for each session, execute once:
  $ in-toto completion fish > ~/.config/fish/completions/in-toto.fish
PowerShell:
  PS> in-toto completion powershell | Out-String | Invoke-Expression
  # To load completions for every new session, run:
  PS> in-toto completion powershell > in-toto.ps1
  # and source this file from your PowerShell profile.


```
in-toto completion [bash|zsh|fish|powershell]
```

### Options

```
  -h, --help   help for completion
```

### SEE ALSO

* [in-toto](in-toto.md)	 - Framework to secure integrity of software supply chains

