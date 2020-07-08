# foundy.test

## Test CLI
```sh
$ echo "feat: a #FE-10" | npx commitlint --verbose
```

## Test 결과 참고

### Local Plugins
[commitlint.js.org - LocalPlugins](https://commitlint.js.org/#/reference-plugins?id=local-plugins)
```sh
TypeError: normalizedName.indexOf is not a function
    at Object.normalizePackageName (/Users/foundy/Development/github-foundy/foundy.test/node_modules/@commitlint/load/lib/utils/plugin-naming.js:31:24)
    at Object.loadPlugin [as default] (/Users/foundy/Development/github-foundy/foundy.test/node_modules/@commitlint/load/lib/utils/load-plugin.js:11:38)
    at config.plugins.forEach (/Users/foundy/Development/github-foundy/foundy.test/node_modules/@commitlint/load/lib/load.js:60:34)
    at Array.forEach (<anonymous>)
    at load (/Users/foundy/Development/github-foundy/foundy.test/node_modules/@commitlint/load/lib/load.js:59:24)
    at process._tickCallback (internal/process/next_tick.js:68:7)
```
* 가이드 예시를 기준으로 로컬 플러그인 시도시 정상 동작이 되지 않는다.

### NPM 게시 Plugins
* 가이드와 같이 `commitlint-plugin-<plugin-name>` 포맷으로 NPM에 게시하여 사용하면 정상 동작이 된다.
