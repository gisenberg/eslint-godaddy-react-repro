## eslint-godaddy-react-repro

This repository is intended to demonstrate an issue with the `eslint-config-godaddy-react` package while running on Windows.

The `eslint` and `gdlint` scripts in `package.json` are intended to illustrate this behavior:

eslint:
```console
C:\Users\gisenberg\git\eslint-godaddy-react-repro (master) (eslint-godaddy-react-repro@1.0.0)
λ npm run eslint

> eslint-godaddy-react-repro@1.0.0 eslint C:\Users\gisenberg\git\eslint-godaddy-react-repro
> eslint src/

C:\Users\gisenberg\git\eslint-godaddy-react-repro (master) (eslint-godaddy-react-repro@1.0.0)
λ
```

gdlint:
```console
C:\Users\gisenberg\git\eslint-godaddy-react-repro (master) (eslint-godaddy-react-repro@1.0.0)
λ npm run gdlint

> eslint-godaddy-react-repro@1.0.0 gdlint C:\Users\gisenberg\git\eslint-godaddy-react-repro
> eslint-godaddy-react src/

C:\Users\gisenberg\git\eslint-godaddy-react-repro\node_modules\.bin\eslint.CMD:1
(function (exports, require, module, __filename, __dirname) { @IF EXIST "%~dp0\node.exe" (

SyntaxError: Unexpected token ILLEGAL
    at exports.runInThisContext (vm.js:53:16)
    at Module._compile (module.js:511:25)
    at Object.Module._extensions..js (module.js:550:10)
    at Module.load (module.js:456:32)
    at tryModuleLoad (module.js:415:12)
    at Function.Module._load (module.js:407:3)
    at Module.require (module.js:466:17)
    at require (internal/module.js:20:19)
    at C:\Users\gisenberg\git\eslint-godaddy-react-repro\node_modules\eslint-config-godaddy\cli.js:41:7
    at C:\Users\gisenberg\git\eslint-godaddy-react-repro\node_modules\which\which.js:87:20

npm ERR! Windows_NT 10.0.14393
npm ERR! argv "C:\\Program Files\\nodejs\\node.exe" "C:\\Program Files\\nodejs\\node_modules\\npm\\bin\\npm-cli.js" "run" "gdlint"
npm ERR! node v6.0.0
npm ERR! npm  v3.8.6
npm ERR! code ELIFECYCLE
npm ERR! eslint-godaddy-react-repro@1.0.0 gdlint: `eslint-godaddy-react src/`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the eslint-godaddy-react-repro@1.0.0 gdlint script 'eslint-godaddy-react src/'.
npm ERR! Make sure you have the latest version of node.js and npm installed.
npm ERR! If you do, this is most likely a problem with the eslint-godaddy-react-repro package,
npm ERR! not with npm itself.
npm ERR! Tell the author that this fails on your system:
npm ERR!     eslint-godaddy-react src/
npm ERR! You can get information on how to open an issue for this project with:
npm ERR!     npm bugs eslint-godaddy-react-repro
npm ERR! Or if that isn't available, you can get their info via:
npm ERR!     npm owner ls eslint-godaddy-react-repro
npm ERR! There is likely additional logging output above.

npm ERR! Please include the following file with any support request:
npm ERR!     C:\Users\gisenberg\git\eslint-godaddy-react-repro\npm-debug.log
```
