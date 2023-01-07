# Yarn Package Manager

## Quickstart
1. `corepack enable`

2. `corepack prepare yarn@stable --activate`

3. New package: `yarn init -p`  
   Existing package: `yarn set version stable`

## Corepack

The preferred way to use yarn is through corepack.

With node 16.10+, corepack is included but you need to opt-in by running `corepack enable`

## Global yarn

When using yarn outside of a package (such as `yarn init`), corepack will default to the activated version.

Set this version using (node 18.6+) `corepack prepare yarn@stable --activate`

## Package yarn

When using yarn inside a package, corepack will check `package.json` for `packageManager` field to determine the version to use. For example,

```js
{
    "packageManager": "yarn@3.3.1"
}
```

For existing packages, run `yarn set version stable` to update package.json

For new packages, run `yarn init -p` to generate a package.json

## .gitignore

For zero-installs, make sure to commit `.pnp.*` and `.yarn/cache`

A normal `.gitignore` looks like this:

```
.yarn/*
!.yarn/cache
!.yarn/patches
!.yarn/plugins
!.yarn/releases
!.yarn/sdks
!.yarn/versions
```

See https://yarnpkg.com/getting-started/qa#which-files-should-be-gitignored for more details

## References

https://yarnpkg.com/getting-started/install

https://github.com/nodejs/corepack

