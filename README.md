# Waytide — code/ruby (retired)

**By [The Eventide Project](https://eventide-project.org)**

**This package moved to [waytide/tools-ruby-lang](https://github.com/waytide/tools-ruby-lang) on 2026-08-21.** This repository is archived and receives nothing further.

## What changed

- **The name and the installed path.** It installs at `waytide/system/tools/ruby-lang/` rather than `waytide/system/code/ruby/`. The grouping names the **tool** a project uses rather than the artifact the rules act on.
- **Where it is authored.** Every other Waytide package is authored in the [composite](https://github.com/waytide/waytide) and published to its own repository by `git subtree split`. This one is authored in its own repository, and nothing splits into it.
- **What it installs.** Its dependency is every other Waytide package, so installing it installs all of Waytide. It is the only package whose dependency is the whole set.

The rules themselves came across unchanged.

## Moving a project to it

```
git rm -r waytide/system/code/ruby

git subtree add --prefix waytide/system/tools/ruby-lang \
  git@github.com:waytide/tools-ruby-lang.git master --squash
```

**Over HTTPS**, where no SSH key is registered, use `https://github.com/waytide/tools-ruby-lang.git` in place of the address above.

**From a bare directory**, one command installs the whole set:

```
curl -O https://raw.githubusercontent.com/waytide/tools-ruby-lang/master/install.sh
sh install.sh
```

## What is still here

The files in this repository are the last state the composite published to it, on 2026-08-21. They are readable and they are not maintained. The record of the move is the composite's migration record, *The Ruby package moves to `tools-ruby-lang`*.

## License

Waytide is licensed under the **Eventide Common Interest License**. It is source-available and free to use. It is not open source in the strict sense, since it does not permit modification. The license text is forthcoming and will be published in `LICENSE`.
