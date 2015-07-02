## Step6: Use Style Guide by ESLint

1. Install eslint and plugins by npm

  ```bash
  npm install --save-dev eslint babel-eslint eslint-plugin-react
  ```

2. make eslint configs

  .eslintrc
  ```json
  {
    "env": {
      "browser": true,
      "node": true
    },
    "rules": {
      "strict": [2, "global"],
      "no-shadow": 2,
      "no-shadow-restricted-names": 2,
      "no-unused-vars": [2, {
        "vars": "local",
        "args": "after-used"
      }],
      "no-use-before-define": 2,
      "comma-dangle": [2, "never"],
      "no-cond-assign": [2, "always"],
      "no-console": 1,
      "no-debugger": 1,
      "no-alert": 1,
      "no-constant-condition": 1,
      "no-dupe-keys": 2,
      "no-duplicate-case": 2,
      "no-empty": 2,
      "no-ex-assign": 2,
      "no-extra-boolean-cast": 0,
      "no-extra-semi": 2,
      "no-func-assign": 2,
      "no-inner-declarations": 2,
      "no-invalid-regexp": 2,
      "no-irregular-whitespace": 2,
      "no-obj-calls": 2,
      "no-reserved-keys": 2,
      "no-sparse-arrays": 2,
      "no-unreachable": 2,
      "use-isnan": 2,
      "block-scoped-var": 2,
      "consistent-return": 2,
      "curly": [2, "multi-line"],
      "default-case": 2,
      "dot-notation": [2, {
        "allowKeywords": true
      }],
      "eqeqeq": 2,
      "guard-for-in": 2,
      "no-caller": 2,
      "no-else-return": 2,
      "no-eq-null": 2,
      "no-eval": 2,
      "no-extend-native": 2,
      "no-extra-bind": 2,
      "no-fallthrough": 2,
      "no-floating-decimal": 2,
      "no-implied-eval": 2,
      "no-lone-blocks": 2,
      "no-loop-func": 2,
      "no-multi-str": 2,
      "no-native-reassign": 2,
      "no-new": 2,
      "no-new-func": 2,
      "no-new-wrappers": 2,
      "no-octal": 2,
      "no-octal-escape": 2,
      "no-param-reassign": 2,
      "no-proto": 2,
      "no-redeclare": 2,
      "no-return-assign": 2,
      "no-script-url": 2,
      "no-self-compare": 2,
      "no-sequences": 2,
      "no-throw-literal": 2,
      "no-with": 2,
      "radix": 2,
      "vars-on-top": 2,
      "wrap-iife": [2, "any"],
      "yoda": 2,
      "indent": [2, 2],
      "brace-style": [2,
        "1tbs", {
        "allowSingleLine": true
      }],
      "quotes": [
        2, "single", "avoid-escape"
      ],
      "camelcase": [2, {
        "properties": "never"
      }],
      "comma-spacing": [2, {
        "before": false,
        "after": true
      }],
      "comma-style": [2, "last"],
      "eol-last": 2,
      "func-names": 1,
      "key-spacing": [2, {
          "beforeColon": false,
          "afterColon": true
      }],
      "new-cap": [2, {
        "newIsCap": true
      }],
      "no-multiple-empty-lines": [2, {
        "max": 2
      }],
      "no-nested-ternary": 2,
      "no-new-object": 2,
      "no-spaced-func": 2,
      "no-trailing-spaces": 2,
      "no-wrap-func": 2,
      "no-underscore-dangle": 0,
      "one-var": [2, "never"],
      "padded-blocks": [2, "never"],
      "semi": [2, "always"],
      "semi-spacing": [2, {
        "before": false,
        "after": true
      }],
      "space-after-keywords": 2,
      "space-before-blocks": 2,
      "space-before-function-paren": [2, "never"],
      "space-infix-ops": 2,
      "space-return-throw-case": 2,
      "spaced-line-comment": 2,
    }
  }
  ```

  src/js/.estlinrc
  ```json
  {
    "parser": "babel-eslint",
    "plugins": [
      "react"
    ],
    "ecmaFeatures": {
      "arrowFunctions": true,
      "blockBindings": true,
      "classes": true,
      "defaultParams": true,
      "destructuring": true,
      "forOf": true,
      "generators": false,
      "modules": true,
      "objectLiteralComputedProperties": true,
      "objectLiteralDuplicateProperties": false,
      "objectLiteralShorthandMethods": true,
      "objectLiteralShorthandProperties": true,
      "spread": true,
      "superInFunctions": true,
      "templateStrings": true,
      "jsx": true
    },
    "rules": {
      "strict": [2, "never"],
      "no-var": 2,
      "react/display-name": 0,
      "react/jsx-boolean-value": 2,
      "react/jsx-quotes": [2, "double"],
      "react/jsx-no-undef": 2,
      "react/jsx-sort-props": 0,
      "react/jsx-sort-prop-types": 0,
      "react/jsx-uses-react": 2,
      "react/jsx-uses-vars": 2,
      "react/no-did-mount-set-state": [2, "allow-in-func"],
      "react/no-did-update-set-state": 2,
      "react/no-multi-comp": 2,
      "react/no-unknown-property": 2,
      "react/prop-types": 2,
      "react/react-in-jsx-scope": 2,
      "react/self-closing-comp": 2,
      "react/wrap-multilines": 2,
      "react/sort-comp": [2, {
        "order": [
          "displayName",
          "mixins",
          "statics",
          "propTypes",
          "getDefaultProps",
          "getInitialState",
          "componentWillMount",
          "componentDidMount",
          "componentWillReceiveProps",
          "shouldComponentUpdate",
          "componentWillUpdate",
          "componentWillUnmount",
          "/^on.+$/",
          "/^get.+$/",
          "/^render.+$/",
          "render"
        ]
      }]
    }
  }
  ```

3. install editor plugin
  - sublime text: Install SublimeLinter & SublimeLinter-eslint
  - atom: Install linter & linter-eslint

### Related links

+ [airbnb javascript style guide](https://github.com/airbnb/javascript)
+ [eslint](http://eslint.org/)
+ [eslint config](http://eslint.org/docs/user-guide/configuring.html)
+ [atom](https://atom.io/)
+ [sublimt text](http://www.sublimetext.com/)