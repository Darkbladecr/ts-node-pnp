# ts-node

Created for the issue: https://github.com/TypeStrong/ts-node/issues/1709

Breaking on initiation of the esm_loader => ts-node/child-loader
`yarn ts-node ./src/index.ts`

```
node:internal/process/esm_loader:94
    internalBinding('errors').triggerUncaughtException(
                              ^

Error [ERR_MODULE_NOT_FOUND]: Cannot find module '/Users/stefan/ts-node/.yarn/__virtual__/ts-node-virtual-645473c738/0/cache/ts-node-npm-10.7.0-ef39b1d45e-2a379e43f7.zip/node_modules/ts-node/child-loader.mjs' imported from /Users/stefan/ts-node/
Did you mean to import /Users/stefan/ts-node/.yarn/__virtual__/ts-node-virtual-645473c738/0/cache/ts-node-npm-10.7.0-ef39b1d45e-2a379e43f7.zip/node_modules/ts-node/child-loader.mjs?
    at new NodeError (node:internal/errors:371:5)
    at finalizeResolution (node:internal/modules/esm/resolve:418:11)
    at moduleResolve (node:internal/modules/esm/resolve:983:10)
    at defaultResolve (node:internal/modules/esm/resolve:1080:11)
    at ESMLoader.resolve (node:internal/modules/esm/loader:530:30)
    at ESMLoader.getModuleJob (node:internal/modules/esm/loader:251:18)
    at ESMLoader.import (node:internal/modules/esm/loader:332:22)
    at initializeLoader (node:internal/process/esm_loader:74:49)
    at loadESM (node:internal/process/esm_loader:87:11)
    at runMainESM (node:internal/modules/run_main:51:21) {
  code: 'ERR_MODULE_NOT_FOUND'
}
```
