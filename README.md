## Usage

The recommended version of [Rubocop](https://github.com/bbatsov/rubocop) to use is `0.49` or higher.

Inside your project, add the `.rubocop.yml` file containing:

```yml
inherit_from:
  - https://raw.githubusercontent.com/blacklane/rubocop/master/rubocop.yml
```

Any project-specific exceptions to the defaults can be appended after this.

When running `rubocop`, the remote configuration file will be cached locally as `.rubocop-https--raw-github...`.
That's why you should make sure to *gitignore* the file:

```
# .gitignore
.rubocop-http*
```

## Contribution

- Make a PR.
- Discuss.
- :shipit:

## Other

- [The list of available cops](https://github.com/bbatsov/rubocop/blob/master/manual/cops.md)
