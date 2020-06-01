powerline-go
============

Compiles and installs [powerline-go](https://github.com/justjanne/powerline-go) and optionally installs handlers for `zsh` and `fish`.

Requirements
------------

None

Role Variables
--------------

* `fish_duration_patch`
  * Type: Boolean
  * Usage: if true, patches powerline-go to remove microseconds. This is because fish's duration is only at the millisecond level.
  * Default: undefined (false)

* `install_fish`
  * Type: Boolean
  * Usage: if true, creates `powerline-go.fish` in `~/.config/fish/fish.d`
  * Default: undefined (false)

* `install_zsh`
  * Type: Boolean
  * Usage: if true, creates `powerline-go.zsh` in `~/.zshrc`
  * Default: undefined (false)

* `modules`
  * Type: string
  * Usage: an optional string of modules to use to override the default configuration of modules
  * Default: undefined (use defaults from powerline-go)

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts:
    - local
  roles:
    - powerline-go
  vars:
    powerline_go:
      install_zsh: true
      install_fish: true
      fish_duration_patch: true
      modules: venv,user,host,ssh,cwd,perms,git,hg,duration,exit,root
```

License
-------

MIT

Author Information
------------------

Patrick Wagstrom &lt;patrick@wagstrom.net&gt;
