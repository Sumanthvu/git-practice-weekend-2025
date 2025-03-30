# Miscellaneous

There some things that are good to know, but not strictly necessary. Here's an (incomplete) list of the ideas. Please feel free to add any 'life hacks' you know/discover to this!

## Clone depth

In old repos, there's usually a lot of history. So, cloning them often takes many GBs, while the actual code you'd like to download(to, for example, browse around) is only a few dozen MBs. To get around this, we can use `git clone --depth 1`.
The `--depth 1` option makes cloning faster by downloading only the latest version of the code instead of the whole history.

 For example,
 `git clone --depth 1 https://github.com/iiitl/git-practice-weekend-2025.git ` takes significantly less time than cloning the entire repo.

## Aliases

There are some commands that we use all the time(for example, `git status`). To avoid typing `status` every single time, we can tell git to interpret `git s` as `git status`. To do this, run

```bash
git config --global alias.s status
```

You can replace `s` with anything other alias.
git config --global alias.co checkout 
git config --global alias.br branch  

 The `--global` flag tells git that we want this setting to be applied everywhere.

## gitconfig

You can make a lot of tweaks to git to make it better. For example, if you misspell commands all the time, you can tell git to autocorrect you and run the command in a couple of seconds:

```bash
git config --global help.autoCorrect 50
```

This will autocorrect your commands(for example, from `git rebaes` to `git rebase`) in 5 seconds and run it.

Some other common options are(thanks @Animeshz for these):

git config --global color.ui auto  
git config --global pull.rebase false

```bash
git config --global user.email <email> # set your default commit email
git config --global user.name <full-name> # set your default commit name
git config --global core.editor code  # use vscode to edit commit messages etc
git config --global core.editor vim  # use vim to edit commit messages etc
git config --global core.editor nano  # use nano to edit commit messages etc

```

A complete list of all configuration options can be found [here](https://git-scm.com/docs/git-config).

## Learn more git

You can go to https://learngitbranching.js.org/ to learn more advanced git topics in a interactive and visual method. Complete the exercises and create a PR with a screenshot showing completed levels. You will get 1 point every 5 exercises, and 4 points for completing all of it.

