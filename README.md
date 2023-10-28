# Example of problems loading xml plugin

## Example with pre-commit

1. Install [pre-commit](https://pre-commit.com/)
2. Run pre-commit on all files

```
❯ pre-commit run --all
prettier.................................................................Failed
- hook id: prettier
- exit code: 1

[error] Cannot find package '@prettier/plugin-xml' imported from /Users/kevin/src/pre-commit-xml-plugin-example/noop.js
```

## Example with installing prettier globally

```
❯ npm install -g prettier @prettier/plugin-xml
…
❯ prettier --plugin=@prettier/plugin-xml example.xml
[error] Cannot find package '@prettier/plugin-xml' imported from /Users/kevin/src/pre-commit-xml-plugin-example/noop.js
```

## Config file

I even tried adding a require statement to `.prettierrc.js`, as mentioned
in [this comment](https://github.com/prettier/prettier/issues/15388#issuecomment-1717746872).

But that doesn't help either.
