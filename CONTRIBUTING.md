# Contributing to lerna-basic

## Getting Started

To get started fork this repository then run:

```sh
git clone git@github.com:${username}/lerna-basic.git
npm install
npm run lerna:bootstrap
```

Since this repository uses [lerna](https://lernajs.io) you'll also need to run `npm run bootstrap` anytime that you have changed the dependencies within a package.

## Commiting changes

Since `lerna-basic` follows the [`conventional-commits`](http://conventionalcommits.org/) standard. Follow these standards: 

1. fix: a commit of the type `fix` patches a bug in your codebase (this correlates with [`PATCH`](https://semver.org/) in Semantic Versioning).
1. feat: a commit of the type `feat` introduces a new feature to the codebase (this correlates with [`MINOR`](https://semver.org/) in Semantic Versioning).
1. BREAKING CHANGE: a commit that has a footer `BREAKING CHANGE:`, or appends a `!` after the type/scope, introduces a breaking API change (correlating with [`MAJOR`](https://semver.org/) in Semantic Versioning). 
A BREAKING CHANGE can be part of commits of any type.
1. types other than `fix:` and `feat:` are allowed, for example @commitlint/config-conventional (based on the the Angular convention) recommends
`build:`, `chore:`, `ci:`, `docs:`, `style:`, `refactor:`, `perf:`, `test:`, and others.
1. footers other than `BREAKING CHANGE: <description>` may be provided and follow a convention similar to git trailer format.

#### Important
Make sure to include the full name of the package that you are changing in the scope part of the commit message in order to get the benefit of 
`lerna` automatically setting the correct version number for the component as well as generating the correct CHANGELOG.

## Releasing and Publishing

lerna-basic uses [lerna](https://lernajs.io) and [github actions](https://github.com/features/actions) in order to publish new versions of packages.

### Release Workflow

1. [User] Checkout release branch `git checkout release/<uniq>`
2. [User] Run `npm run lerna:version`
3. [User] Submit Release Pull Request
4. [Moderators] Review Release Pull Request
5. [Moderators] Merge Pull Request when Approved
6. [Actions] Publish Packages

## Resources
Here is a list of the underlined tools/methodology being used to maintain this repo.

* [Lerna](https://lernajs.io)
* [Semantic Versioning](https://semver.org/)
* [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
* [Github Actions](https://github.com/features/actions)
