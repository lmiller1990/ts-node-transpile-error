Discovered while working on https://github.com/cypress-io/cypress/issues/26148

- ✅ Works: `NODE_OPTIONS="--loader ts-node/esm" node index.ts`
- ❌ Does not work: `NODE_OPTIONS="--loader ts-node/esm/transpile-only" node index.ts`

Error:

```
(node:10336) ExperimentalWarning: Custom ESM Loaders is an experimental feature. This feature could change at any time
(Use `node --trace-warnings ...` to show where the warning was created)
/Users/lachlanmiller/code/dump/tsnode/node_modules/ts-node/src/index.ts:859
    return new TSError(diagnosticText, diagnosticCodes, diagnostics);
           ^
TSError: ⨯ Unable to compile TypeScript:
error TS5096: Option 'allowImportingTsExtensions' can only be used when either 'noEmit' or 'emitDeclarationOnly' is set.
```
