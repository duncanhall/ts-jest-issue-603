# Exaxmple repo for [ts-jest issue #603](https://github.com/kulshekhar/ts-jest/issues/603)

This repo provides the minimum possible setup for reproducing [ts-jest issue #603](https://github.com/kulshekhar/ts-jest/issues/603)

### Run the tests 

```
yarn install
yarn test
```

### Result
```
➜  ts-jest-issue CI=true yarn test
yarn run v1.7.0
$ react-scripts-ts test --env=jsdom
FAIL src/__tests__/App.test.tsx
  ● Test suite failed to run

    TypeError: require(...).install is not a function

    > 1 | import * as React from 'react';
      2 | import * as ReactDOM from 'react-dom';
      3 | import App from '../App';
      4 |

      at Object.<anonymous> (src/__tests__/App.test.tsx:1:122)

Test Suites: 1 failed, 1 total
Tests:       0 total
Snapshots:   0 total
Time:        1.921s
Ran all test suites.
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.

```

