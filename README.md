# ReactJS playground

# [Udemy](https://www.udemy.com/)

## [React - The Complete Guide (incl Hooks, React Router, Redux)](https://www.udemy.com/course/react-the-complete-guide-incl-redux/)

#### Section 1

---

#### Section 2

---

[18. The Spread & Rest Operator](https://www.udemy.com/course/react-the-complete-guide-incl-redux/learn/lecture/8211796#overview)

- `...`

---

# [Frontend Masters](https://frontendmasters.com/)

## [Complete Intro to React, v5 - Brian Holt](https://frontendmasters.com/courses/complete-react-v5/)

#### Introduction

```
- Introduction
- Project setup
     > Import React and ReactDOM CDN in script tag.
     > explain why ReactDOM needs to import
- A note on course font
     > how to customize VSCode fonts
```

---

#### Pure React

```
- Getting started with pure React
     > basic understanding of components
- createElement arguments
     > understading of arguments
- Reusable components
- Passing in component Props
     > Props = properties
- Destructuring props
     > for reusability
```

---

#### Tools

```
- NPM and generating a package.json file
     > Node Package Manager
     > This is going to allow us to, rather than just loading node off of the CDN,
       we're gonna actually install it off of the registry and build our project.
       So that it's actually included with the package, and we don't have to rely on unpackage to be up,
       right?
     > Unpackage is really good for just like testing things out. But do not rely on it
       for production traffic, cuz then you're at their mercy, okay?
     > install node -- https://nodejs.org/en/
     > $ npm init
          >> initiate NPM project
- Prettier
     > `$ npm install -D prettier`
          >> -D used to indicate install in development environment only
          >> "install" can be replaced by "i" ($ npm i -D prettier)
- NPM scripts
     > run commands inside "scripts" key in package.json file.
     > `$ prettier --write` option will apply prettier format to files.
     > this can be run by doing `$ npm run <script_key>`.
- Prettier setup
     > make sure enabled below VSCode settings.
          >> format on save
          >> require config
               -- need to create `.prettierrc` in project root directory for the config.
- ESlint setup
     > `$ npm install -D eslint eslint-config-prettier`
     > difference between prettier and eslint
          >> Prettier is purely concerned with is there a space here? Is there return here? How does this
             file star, it's very mechanical. It doesn't care about what the code actually does, So it
             doesn't look like does this variable exist? are we using the wrong method here? Are we
             using old JavaScript here?
          >> Eslint is much more concerned with style, right. It's concerned with what methods are you using?
             You know, accessibility friendly, right? It can check kind of those things.
     > .lock file
          >> when you deploy your code to production, it's actually locked down the versions. If you look at
             this you can see that it has integrity checks, and like where to download it from and what 
             version it's on and stuff like that. And you want it to have this, because now I can install 
             exactly the correct versions in productions. So, what I'm running in my computer, is exactly 
             what's running on production
          >> `$ npm ci`
               -- It'll use the package lock file to install the version in that file
          >> while `$ npm install`
               -- uses the package.json file for the version to install
- ESlint configuration
     > Add `{"extends": [...]}` in .eslintrc.json file.
     > Add eslint command in package.json "scripts".
          >> `"lint": "eslint \"src/**/*.{js,jsx}\" --quiet"`
- gitignore
     > disable git on tracking changes to files 
     > ignore below files
          >> node_modules/
          >> .DS_Store
          >> .cache/
          >> dist/
          >> coverage/
          >> .vscode/
          >> .env
- Parcel
     > Bundler package
          >> A bundler helps web developers manage a group of tools that solve related problems. You can
             think of it as a “meta-tool,” where each sub-tool is managed by a plugin. Although bundlers
             can be used to do all kinds of fancy stuff, we will focus on three sets of problems here that
             apply to any web development project.
               -- Transpiling higher-level languages into HTML, CSS and JavaScript
               -- Serving files on an ad-hoc HTTP server with live-reloading
               -- Preparing the application for production: minify, concatenate, uglify
          >> ref: https://medium.com/fusebox/beginner-web-developers-use-a-bundler-31ab0c91d2f5
     > https://parcel.org
          >> easier to use
          >> `$ npm install -D parcel-bundler`
               -- this will be going in "node_modules/.bin/` folder
          >> add another command in "scripts" key in  package.json file.
     > Webpack
          >> another bundler package
          >> powerful package but difficult to setup and complex
     > Grunt, Gulp, Brunch, Browserify, Rollup
          >> another bundler packages
- Installing React and ReactDOM
     > `$ npm install react react-dom
          >> notice that `-D` is not used because it is not needed here for this is production dependencies
     > other VSCode extension tools:
          >> eslint
          >> npm intellisense
- Separate App into Modules
     > Useful shortcut command to select block of code and move it to a new file.
     > VSCode action
          >> highlight a codes in the file
          >> click the bulb icon
          >> select move to a new file option
          >> voila!
```
---

#### JSX

```
- Converting to JSX
     > Babel -- library
     > returning a HTML React tag
     > VSCode extension -- Javascript React
          >> Or change the file extension to jsx
          >> .jsx extension is not neccessary according to React team.
- Configuring ESLint for React
     > `$ npm install -D babel-eslint eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react`
     > `prettier` and `prettier/react` in eslintrc.json file should be in the end of the list
     > add this also in "extends" key in eslintrc.json file
          >> "plugin:import/errors"
          >> "plugin:react/recommended"
          >> "plugin:jsx-a11y/recommended"
     > update "plugins" key in eslintrc.json file
          >> "react"
          >> "import"
          >> "jsx-a11y"
               -- more about accessibility
     > update "rules" key in eslintrc.json file
          >> "react/prop-types" : 0  # turn off
               -- very week prop type checking 
          >> "no-console": 1  # turn on
     > Add "settings" key in eslintrc.json file
          >> "react": {"version": "detect"}
               -- tell eslint to what React version to use.
- JSX Composite Components & Expressions
     > `return ();` parenthesis are used here for block of codes or codes with break lines.
     > `<tag />` "/" is required in JSX.
     > in JSX you can use <div />
     > `{}` Javascript expression
```
---

### Hooks

```
- Creating a Search Component
     > Class syntax?
- Setting State with Hooks
- Best Practices for Hooks
- Configuring ESLint for Hooks
- Calling the Pet API
- Unique List item Keys
- Breed Dropdown
- Custom Hooks
```

## NOTES:

```
1. class component
2. functional component
     - good, easy to test, easy to predict,  has less overhead as opposed to classes (Rob)
     - pure vs impure functions? (Rob)

- classes should only be used if you're dealing with stateful components
- functional can do stateful now
- useEffect

- hook
- context


- but, hooking the context, makes the code less complicate
```
