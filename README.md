# npm-workspaces-example

Repro for an issue with hoisting from an npm workspace

## Steps to repro

1. Clone the repo
2. Run `npm install`
3. Observe modules are properly hoisted to `./node_modules`
4. Modify `packages/package-a/package.json` to use `"@github/memoize": "1.1.4"`
5. Run `npm install` again
6. Observe the new version is installed in `packages/package-a/node_modules/@github/memoize`
