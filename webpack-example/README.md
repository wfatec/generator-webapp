# AMS For DG5

## Introduction

<div align="justify">This project is based on DRC starter kit, DRC starter kit is a environment for establishing your project quickly. There are many build-in features, like scaffolding, hot-reload, code splitting etc. If you want to adjust starter kit for fit your scenario, it retains many flexibility for you. </div>

## DRC starter kit

[![build status](http://10.120.129.20/react/drc-starter-kit/badges/master/build.svg)](http://10.120.129.20/react/drc-starter-kit/commits/master).
[![coverage report](http://10.120.129.20/react/drc-starter-kit/badges/master/coverage.svg)](http://10.120.129.20/react/drc-starter-kit/commits/master)

**For more information, please visit our gitbook: [http://10.136.225.86:3003/book/drc-starter-kit/](http://10.136.225.86:3003/book/drc-starter-kit/)**

## Features of DRC starter kit

*  馃憦 **Hot reloading**
*  馃憦 **Scaffolding**
*  馃憦 **Code splitting**
*  馃憦 **Redux devtool is supported**
*  馃憦 **Integration with lint testing, unit testing and coverage testing**
*  馃憦 **Integration with browser compatibility**
*  馃憦 **Multi style loader supported**
*  馃憦 **Integration complex settings with one file**
*  馃憦 **Nice flexibility for extension**
*  馃憦 **Using modern plug-ins (React-router, React etc.)**


## Requirements

node \^5.0.0

yarn \^0.23.0 or npm \^3.0.0

## Installation

Now, you can clone our repo by:
```
git clone http://10.120.137.178/wfatec/AMS-dg5.git
```

Then, you need to install some dependencies:
```
cd AMS-DG5;
npm install  # Install project dependencies (or `yarn install`)
```
It's done!

## Running the Project

After completing the installation step, you're ready to start the project!

```
npm start  # Start the development server (or `yarn start`)
```

While developing, you will probably rely mostly on npm start; however, there are additional scripts at your disposal:

|      Script (also yarn)       |                     Description                           |
|:------------------|:----------------------------------------------------------------------|
|     npm start     |  Start compile your project. The default serve url would be: http://localhost:3000|
|   npm run quick   |  Call scaffolding to generate template file                           |
|   npm run build   |  build your project as production (minify, hash etc). The default output root is dist|
|   npm run test    |  Testing your codes. This command will run lint testing and unit testing at same time|
| npm run test:unit |  Run unit testing alone                                               |
| npm run test:unit:watch | Run unit testing in watching mode (Trace your changing in testing immediately)|
| npm run test:lint |  Run lint testing alone                                               |
| npm run test:lint:fix | Run lint testing with automatically fixing errors                 |
| npm run test:lint:report | Run lint testing and output result as a report. The default path of report is reports |
| npm run test:coverage | Run coverage testing and output report in reports directory       |
| npm run release |  Release your codes with test, build. If passed, the version tag and codes will be pushed into repo|

Besides, there are many options you can attach after your command:

|    Option       |                              Description                                    |
|:----------------|:----------------------------------------------------------------------------|
|   --indir       | The entry directory of your main codes in your project. Default is `src`.   |
|   --main        | The file name of the application's entry point. Default is `main`           |
|   --outdir      | The name of the directory in which to emit compiled assets. Default is `dist`|
|   --testdir     | The name of the testing entry directory. Default is `tests`                 |
|   --reportdir   | The name of the testing output report directory. Default is `reports`       |
|   --template    | The template of html. It will be used if the configuration of html is true. Default is index.html|
|   --port        | The port of the server. Default is 3000.                                    |
|   --publicpath  | The base path for all projects assets (relative to the website root). Default is '/'|
|   --sourcemaps  | Whether to generate sourcemaps. Default is false                            |
|   --externals   | A hash map of keys that the compiler should treat as external to the project. Default is {}|
|   --globals     | A hash map of variables and their values to expose globally. Default is {}  |
|   --outputlint  | Whether to output the lint report. Default is false.                        |
|   --fixlint     | Whether to fix the lint error automatically. Default is false.              |
|   --verbose     | Whether to enable verbose logging. Default is false.                        |
|   --dsiableless | Whether to disable less loader. Default is false.                           |
|   --dsiablecss  | Whether to disable css loader. Default is false.                            |
|   --dsiablescss | Whether to disable scss loader. Default is false.                           |
|   --dsiabletext | Whether to disable text loader. Default is false.                           |
|  --dsiableimage | Whether to disable image loader. Default is false.                          |
|   --dsiablefont | Whether to disable font loader. Default is false.                               |
|   --dsiablehtml | Whether to disable html loader. Default is false.                               |
|   --polyfill    | Assign the location of polyfill. By default, the babel-polyfill will be used.|
|   --imagesize   | The limit of image size. Default is 8192.                                   |
|   --fontsize    | The limit of font size. Default is 10000.                                   |
|   --threshold   | The setting of the coverage threshold. Default is { statements: 50, branches: 50, functions: 50, lines: 50}|
|   --vendors     | The list of modules to bundle separately from the core application code.    |

All of default setting can be modified in project.config.js of root.

## Project structure

The project structure is designed by functionality of Redux-React. For more introduction of this structure can visit the offical website of Redux: [connect](hhttps://redux.js.org/docs/introduction/LearningResources.html). If you want to modify the folder structure, please feel free to do that. There is no constraint in project structure of our starter kit.

```
.
鈹溾攢鈹€ build                      # All build-related code
鈹?  |鈹€鈹€ configs                # All configuration files
鈹?  鈹?  鈹溾攢鈹€ jest.config.js     # The configuration of Jest
鈹?  鈹?  鈹斺攢鈹€ postcss.config.js  # You can put your settings here to do some post css prefix
鈹?  |鈹€鈹€ lib                    # All libraries used in scripts
鈹?  鈹?  鈹溾攢鈹€ logger.js          # A logger script for printing pretty log
鈹?  鈹?  鈹斺攢鈹€ path.js            # A path script for handling path issue in script
鈹?  |鈹€鈹€ scaffold               # All Scaffold setting files and script files
鈹?  鈹?  鈹溾攢鈹€ **                 # Template of scaffolding
鈹?  鈹?  鈹溾攢鈹€ start.js           # The entry point of scaffold script
鈹?  鈹?  鈹斺攢鈹€ validate.js        # A script for checking if file is exised
鈹?  |鈹€鈹€ scripts                # All build-related scripts
鈹?  鈹?  鈹溾攢鈹€ compile.js         # A script for handling code compiling
鈹?  鈹?  鈹溾攢鈹€ eslint.js          # A script for handling lint checking
鈹?  鈹?  鈹斺攢鈹€ start.js           # A script for starting building server
鈹?  |鈹€鈹€ server                 # Express application that provides webpack middleware
鈹?  鈹?  鈹斺攢鈹€ main.js            # Server application entry point
鈹?  鈹斺攢鈹€ webpack.config.js      # Configuration of webpack
鈹溾攢鈹€ public                     # Static public assets (not imported anywhere in source code)
鈹溾攢鈹€ src                        # Application source code
鈹?  鈹溾攢鈹€ actions                # All of business logics for components
鈹?  鈹溾攢鈹€ assets                 # Fonts, images, svgs, csvs etc. All kinds of files used in pages.
鈹?  鈹溾攢鈹€ components             # Global reusable components
鈹?  鈹溾攢鈹€ containers             # Global reusable container components
鈹?  鈹溾攢鈹€ hocs                   # Global reusable higher order components
鈹?  鈹溾攢鈹€ layouts                # Components that dictate major page structure
鈹?  鈹溾攢鈹€ models                 # Data structure definition of reducer
鈹?  鈹溾攢鈹€ reducers               # A center to decide how to update state
鈹?  鈹溾攢鈹€ routes                 # Main route definitions and async split points
鈹?  鈹溾攢鈹€ store                  # Redux-specific pieces
鈹?  鈹?  鈹斺攢鈹€ createStore.js     # Create and instrument redux store
鈹?  鈹溾攢鈹€ index.html             # Main HTML page container for app
鈹?  鈹斺攢鈹€ main.js                # Application bootstrap and rendering
鈹斺攢鈹€ tests                      # Unit tests
```

## Create you own scaffolding

Allows you to auto-generate boilerplate code for common parts of your application. Feel free to modify or create a new template in `build/scaffold`.

## Testing

To add a unit test, create a `.spec.js` file anywhere inside of `./tests`. Jest and webpack will automatically find these files, and Enzyme will be available within your test without the need to import them.

## Maintainers

<table>
  <tbody>
    <tr>
      <td align="center">
        <a href="http://10.120.129.20/chuck.wu">
          <img width="150" height="150" src="http://10.120.129.20/uploads/-/system/user/avatar/36/avatar.png">
          </br>
          chuck.wu
        </a>
      </td>
      <td align="center">
        <a href="http://10.120.137.178/wfatec">
          <img width="150" height="150" src="http://www.gravatar.com/avatar/fe60162e396e15b275aa27c3f4af5182?s=800&d=identicon">
          </br>
          chao.wang
        </a>
      </td>
    </tr>
  <tbody>
</table>
