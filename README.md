# React Storybork

An example repo of Storybook breaking React.

Will update when I have a fix.

## To reproduce

```console
$ npx create-react-app react-storybork
$ cd react-storybork
$ yarn start # still works
$ npm install -g @storybook/cli@alpha # install alpha version
$ sb -V # verify
4.0.0-alpha.25
$ sb init

 • Detecting project type. ✓
 • Adding storybook support to your "Create React App" based project. ✓
 • Preparing to install dependencies. ✓

yarn install v1.10.1
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
warning " > babel-loader@8.0.4" has unmet peer dependency "webpack@>=2".
warning "@storybook/react > @emotion/styled > @emotion/styled-base@0.10.6" has unmet peer dependency "@emotion/core@0.x.x".
[4/4] 📃  Building fresh packages...
success Saved lockfile.
✨  Done in 10.62s.

 • Installing dependencies. ✓

To run your storybook, type:

   yarn storybook

For more information visit: https://storybook.js.org
$ yarn start
Failed to compile.

./src/index.js
Error: [BABEL] /Users/booyaa/Documents/Coding/madetech/learntech/coreskills/webappdev/owl/react-storybork/src/index.js: Cannot find module '@babel/plugin-syntax-jsx' (While processing: "/Users/booyaa/Documents/Coding/madetech/learntech/coreskills/webappdev/owl/react-storybork/node_modules/babel-preset-react-app/index.js$1$0")
```

## To fix

```console
rm -rf react-storybork
git clone git@github.com:booyaa/react-storybork.git
yarn install
yarn start # woohoo! Also storybook and jest are working too.
```