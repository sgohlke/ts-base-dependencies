# ts-base-dependencies
Collection of dependencies for NodeJS Typescript projects

**Deprecation notice**:
This package will no longer be maintained. You can now use Dependabot group feature to group dependency updates so this approach is not necessary anymore.

Contains dependencies that can be used as **devDependencies** to work with a Typescript project containing Eslint for linting and Jest for testing. For the list of included dependencies see [package.json](https://github.com/sgohlke/ts-base-dependencies/blob/main/package.json). The dependencies have fixed versions, they are updated by Dependabot automatic dependency updates.

# Setup NodeJS Typescript project

1. Install NodeJS
2. Change to your application folder
3. Run `npm init -y`. This will initialize the NodeJS project and create a package.json file.
4. Run `npm i -D @sgohlke/ts-base-dependencies`. This will install the necessary devDependencies.
5. Run `npx tsc --init` or copy the [tsconfig.json](https://github.com/sgohlke/ts-base-dependencies/blob/main/tsconfig.json) file from this project to your project.
6. Run `npx ts-jest config:init` or copy the [jest.config.js](https://github.com/sgohlke/ts-base-dependencies/blob/main/jest.config.js) and [jest.setup.ts](https://github.com/sgohlke/ts-base-dependencies/blob/main/jest.setup.ts) files from this project to your project.
7. Run `npm init @eslint/config`. When asked if you want to use Typescript answer "yes". Or copy the [.eslintrc.json](https://github.com/sgohlke/ts-base-dependencies/blob/main/.eslintrc.json) file from this project to your project.
8. Create "src" folder
9. Change "package.json" scripts to contain the scripts below.
10. Add the files in the "src" file.
11. To test eslint works add some unused variable and run `npm run lint`. This should indicate that unused code is found.
12. To test jest works add a test file and run `npm test`. This should run the test and show the test result.

Scripts in package.json file:
```json
"scripts": {
    "check": "tsc --noEmit --pretty",
    "lint": "eslint src/*.ts",
    "test": "jest"
}
```

# Keep dependencies up-to-date

You can update all dependencies included in this project/"library" at once by updating to a new version of **@sgohlke/ts-base-dependencies**.
