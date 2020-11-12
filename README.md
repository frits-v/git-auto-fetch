Copied from
https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git-auto-fetch with minor
changes to adapt to `prezto`

# Git auto-fetch

Automatically fetches all changes from all remotes while you are working in git-initialized directory.

#### Usage

1. Clone this repo in your zprezto-contrib folder (eg ~/.zprezto-contrib)
```shell
cd ~/.zprezto-contrib && git clone git@github.com:frots/git-auto-fetch.git
```
1. Add module to your prezto pmodule line:
```shell
zstyle ':prezto:load' pmodule \
  'environment' \
  'terminal' \
  'etc...' \
  'git-auto-fetch'
```

Every time you launch a command in your shell all remotes will be fetched in background.
By default autofetch will be triggered only if last fetch was done at least 60 seconds ago.
You can change fetch interval in your .zpreztorc:
```shell
zstyle ':prezto:module:git-auto-fetch' interval 60
```
Log of `git fetch --all` will be saved into `.git/FETCH_LOG`


#### Toggle auto fetch per folder
If you are using mobile connection or for any other reason you can disable git-auto-fetch for any folder:

```shell
$ cd to/your/project
$ git-auto-fetch
disabled
$ git-auto-fetch
enabled
```
