# Changelog

All notable changes to this project will be documented in this file.

## [3.0.2]

- [#1](https://github.com/kufu/textlint-plugin-ruby/pull/1) Change repository owner from @alpaca-tc to @kufu
  - Add eslint, huscky as so on
  - Change CI from CircleCI to GithubActions

## [3.0.1]

- [#2](https://github.com/alpaca-tc/textlint-plugin-ruby/pull/2) Fixed a bug that a lot of textlint-ruby processes were booted when running textlint with --fix option.

## [3.0.0]

- The parsing process has been optimized. Currently, `textlint-ruby` starts up as a communication process and uses the process as long as you are using textlint.

### Breaking Changes

- If you set execCommand, options requires "--stdout" option.

```
# NG
{
  "plugins": {
    "ruby": {
      "execCommand": ["textlint-ruby"]
    }
  }
}

# OK
{
  "plugins": {
    "ruby": {
      "execCommand": ["textlint-ruby", "--stdio"]
    }
  }
}
```

- Requires textlint-ruby >= 2.0.0
 
## [1.0.0]

- First release
