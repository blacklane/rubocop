## Usage

The recommended version of [Rubocop](https://github.com/bbatsov/rubocop) to use is `0.49` or higher.

Inside your project, add the `.rubocop.yml` file containing:

```yml
inherit_from:
  - https://raw.githubusercontent.com/blacklane/rubocop/master/rubocop.yml
```

Any project-specific exceptions to the defaults can be appended after this.

When running `rubocop`, the remote configuration file will be cached locally as `.rubocop-https--raw-github...`. That's why you should make sure to *gitignore* the file:

```
# .gitignore

.rubocop-http*
```

## Cache

If you see style errors in CI that you can't reproduce locally, that's probably because of the cached `.rubocop-https--raw-github...` file. You'll need to remove it, ideally whenever the `rubocop.yml` file inside this repository changes.

## Contribution

- Keep the rules and their settings sorted alphabetically.
- Make a PR.
- Discuss.
- :shipit:

## Other

- [The list of available cops](https://github.com/bbatsov/rubocop/blob/master/manual/cops.md)
- [Pronto: A gem for running Rubocop only on the git changes](https://github.com/prontolabs/pronto)
