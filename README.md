# Grain NEAR SDK

This project provides bindings to the [NEAR](https://near.org) SDK in order to enable easy writing of NEAR smart contracts in Grain.

## Generating the Documentation

```bash
$ find src -name '*.gr' | xargs -L 1 -I '{}' bash -c 'grain doc {} > $(echo {} | sed "s:src:docs/generated:g" | sed "s/\\.gr/.md/g")'
```

# Building the Tests

Due to an [NPM Bug](https://github.com/npm/cli/issues/4774), this project requires `npm@8.4.0` to build.

To run the test suite, the following is needed in order to install all of the nested dependencies:

```bash
$ (npm ci && cd test-suite && npm ci && cd example-contracts && npm ci)
```

Then, to run the tests, you can simply run

```bash
$ npm run test
```
