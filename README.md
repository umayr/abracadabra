# Abracadabra
> Helps you keep your code less crazy by adding either eslint or jshint in the pre-commit hooks.

## Usage

In your project root directory, type:
```
  $ npm install --save-dev abracadabra
```

and that's it. 

## FAQ

#### What does it actually do?

Upon installation it adds a git pre-commit hook in your repository, which runs every time you're going to commit something. In this case it'll run a npm task that validates your code either via `eslint` or `jshint`. In that way, anybody in your team can't commit anything that doesn't match the standards.

#### What does it use for linting?

It's up to you. If you don't have any `eslint` or `jshint` configurations in your root directory, it'll ask you and then create a default configuration for linter of your choice. You may later change configurations according to your needs.

#### How it is different from [this](https://github.com/nlf/precommit-hook)?

There are two major differences, one being that `nlf/precommit-hook` only supports `jshint` and has it in its dependencies, while `abracadabra` supports `jshint` as well as `eslint` moreover it uses the lint command from your dependencies. Plus, it has quite verbose default configuration files. Other than that, it uses the same [`nlf/git-validate`](https://github.com/nlf/git-validate/) module under the hood as `precommit-hook`.

#### Default configurations?

Here they are; [`.eslintrc`](https://github.com/umayr/abracadabra/blob/master/templates/.eslintrc) & [`.jshintrc`](https://github.com/umayr/abracadabra/blob/master/templates/.jshintignore).

#### I need to commit a hotfix, how do I bypass the linting?

You can bypass the pre-commit hook by:
```bash
 $ git commit --no-verify
```
