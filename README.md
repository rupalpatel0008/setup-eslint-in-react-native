# How to setup eslint in a react-native project
**Step 1:** Install eslint, babel-eslint, eslint-plugin-react and eslint-plugin-react-native
  * npm install --save-dev eslint babel-eslint eslint-plugin-react eslint-plugin-react-native
  
**Step 2:** Initialize eslintrc file for your project
  * cd to your project
  * node_modules/.bin/eslint --init: This will ask following questions.
    * ? How would you like to configure ESLint?
      > Answer questions about your style
    * ? Which version of ECMAScript do you use?
      > ES2018
    * ? Are you using ES6 modules?
      > Yes
    * ? Where will your code run?
      > ◉ Browser
    * ? Do you use CommonJS?
      > Yes
    * ? Do you use JSX?
      > Yes
    * ? What style of indentation do you use?
      > Spaces
    * ? What quotes do you use for strings?
      > Single
    * ? What line endings do you use?
      > Unix
    * ? Do you require semicolons?
      > Yes
    * ? What format do you want your config file to be in?
      > JavaScript
   *This will create a .eslintrc.js file for your project
