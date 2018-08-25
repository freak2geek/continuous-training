# Jest

Jest is a test infrastructure which features in:

- Zero configuration testing platform. Complete and ready to set-up JavaScript testing solution.

- Fast interactive watch mode runs only test files related to changed files and is optimized to give signal quickly.

- Capture snapshots of React trees or other serializable values to simplify testing and to analyze how state changes over time.

- Jest parallelizes test runs across workers to maximize performance. Console messages are buffered and printed together with test results. Sandboxed test files and automatic global state resets for every test so no two tests conflict with each other.

- Easily create code coverage reports using --coverage. No additional setup or libraries needed! Jest can collect code coverage information from entire projects, including untested files.

- Powerful mocking library for functions and modules.

## Test conventions

- Use `__tests__` directories to allocate tests for all modules of a given directory. Jest by default searches all these directories.

- Use `__mocks__` directory to keep the mocks of local modules, npm module or a node module. Turn it on in the Jest configuration.

## Test environment

- Use `jest-cli` to run tests directly.

- Test discover strategy: `__tests__/` folders and `.(test|spec).js` files.

- Jest includes the browser environment already available. It can be turned off by establishing in a configuration `testEnvironment: "node"`.

- Use `babel-jest` to ensure the babel parses correctly.

- Use interactive mode.

    1 - `--watch`. run tests since the last commit.

    2 - `--watchAll`. run all tests.

- Use `--coverage` to get a report of test code coverage.

    1 - `collectCoverageFrom`, to skip test files.

    2 - `coverageThreshold`, ensure better coverage.

- Snapshot, `expect(output).toMatchSnapshot`. The snapshot are genrated automatically within `__snapthots__/` folder.

## References

- Check out: [Jest site](https://jestjs.io/)

- Watch: Jest basic course: [1](https://egghead.io/lessons/javascript-test-javascript-with-jest), [2](https://egghead.io/lessons/javascript-add-babel-integration-with-jest), [3](https://egghead.io/lessons/typescript-getting-started-with-jest-using-typescript), [4](https://egghead.io/lessons/javascript-use-jest-s-interactive-watch-mode), [5](https://egghead.io/lessons/javascript-track-project-code-coverage-with-jest) and [6](https://egghead.io/lessons/javascript-use-jest-s-snapshot-testing-feature).
