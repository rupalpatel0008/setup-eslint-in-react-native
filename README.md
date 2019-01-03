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
   
 **Step 3:** Update the .eslintrc.js file
  * Add "plugin:react/recommended" for the "extends" property
   > "extends": ["eslint:recommended", "plugin:react/recommended"]
  * Use babel-eslint as the parser
   > "parser": "babel-eslint",
  * Add the property "experimentalObjectRestSpread" inside "ecmaFeatures"
   > `"ecmaFeatures": {
      "jsx": true,
      "modules": true,
      "experimentalObjectRestSpread": true
    }`
  * Add sourceType inside the parserOptions
   > `"parserOptions": {
       ...
       "sourceType": "module"
      },`
  * Use plugin react
   > `"plugins": [
        "react"
       ],`
  * Add some rules that you need
   > Refer the example .eslintrc.js
  * Add globals that are required
   > Refer the example .eslintrc.js
  * Add the property "settings"
   > `settings: {
       react: {
        version: require('./package.json').dependencies.react,
       }
      }`
      
**Step 4:** Use eslint by adding some scripts in your package.json
 * To lint:
   > "lint": "eslint ./App"
   > Run this script by npm run lint
 * To fix code:
   > "fixcode": "eslint --fix ./App"
   > Run this script by npm run fixcode
 * To run lint before you run your app in ios/android
   *> For ios: "ios": "npm run lint && react-native run-ios"
   *> Run this script by: npm run ios
   
   *> For android: "android": "npm run lint && react-native run-android"
   *> Run this script by: npm run android

       
