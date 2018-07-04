# Exaxmple repo for [ts-jest issue #603](https://github.com/kulshekhar/ts-jest/issues/603)

This repo provides the minimum possible setup for reproducing [ts-jest issue #603](https://github.com/kulshekhar/ts-jest/issues/603)

### Run the tests 

```
yarn install
CI=true yarn test
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

### Notes
This issue appears in ts-jest@23.0.0 - if you downgrade to the previous version, the issue goes away:

```
yarn upgrade ts-jest@22.4.2
CI=true yarn test 
```

Gives the expected result:

```
yarn run v1.7.0
$ react-scripts-ts test --env=jsdom
PASS src/__tests__/App.test.tsx
  ✓ renders without crashing (23ms)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        2.004s
Ran all test suites.
Done in 3.59s.
```


