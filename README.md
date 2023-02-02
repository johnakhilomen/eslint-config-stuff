# eslint-config-stuff
ES-Lint config stuff


# VSCode - ESLint, Prettier & Airbnb Setup

### 1. Install ESLint & Prettier extensions for VSCode

Optional - Set format on save and any global prettier options

### 2. Install Packages
```
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node
```

```
npx install-peerdeps --dev eslint-config-airbnb
```

### 3. Create .prettierrc for any prettier rules (semicolons, quotes, etc)

### 4. Create .eslintrc.json file (You can generate with eslint --init if you install eslint globally)

```
{
  "extends": ["airbnb", "prettier", "plugin:node/recommended"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "no-unused-vars": "warn",
    "no-console": "off",
    "func-names": "off",
    "no-process-exit": "off",
    "object-shorthand": "off",
    "class-methods-use-this": "off"
  }
}
```

### Reference
* ESLint Rules - https://eslint.org/docs/rules/
* Prettier Options - https://prettier.io/docs/en/options.html
* Airbnb Style Guide - https://github.com/airbnb/javascript

#_


# define is not defined
In your .eslintrc.json set:
```python
"env": {
    "amd": true
},
```

# module, global, setImmediate, exports is not defined
```
"env": {
    "node": true
},
```

# jQuery eslint config
```python
module.exports = {
    "env": {
        "browser": true,
        "commonjs": true,
        "es2021": true,
        "jquery":true,
        "amd":true
    },
    "extends": "eslint:recommended",
    "parserOptions": {
        "ecmaVersion": 12
    },
    "rules": {
    }
};
```

## Usage

```sh
npm install --save-dev eslint-config-jquery
```

Configure ESLint with a `.eslintrc` file using the following contents:
```json
{
	"extends": "jquery"
}
```
# disable lint:

The // eslint-disable-line comment disables the no-eval rule for just that line. You can also disable the no-eval rule for an entire function block by using /* eslint-disable */ . If you put /* eslint-disable no-eval */ before any code in a . js file, that will disable the no-eval rule for the entire file

# Downloads
To download VSCode:
https://code.visualstudio.com/

To download nodejs:
https://nodejs.org/en/

The commands used in the recording:
npm init
npm install -g eslint
eslint --init
eslint js

# Fixes
Change `isPrototypeOf` to `isPrototypeOf.call`
Change `hasOwnProperty` to `hasOwnProperty.call`


## Setting up Eslint for Typescript
To install ESLint and airbnb plugin
```python
npm install --save-dev eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-config-airbnb 

// or with yarn:
yarn add --dev eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-config-airbnb

```

To configure ESLint, you can define the configuration in the .eslintrc.json and would look something like:
```

{
  "extends": [
    "eslint:recommended",
    "plugin:@typescript-eslint/recommended",
    "airbnb"
  ],
  "parser": "@typescript-eslint/parser",
  "plugins": ["@typescript-eslint"],
  "rules": {
    "@typescript-eslint/indent": ["error", 2],
    "@typescript-eslint/no-unused-vars": "error",
    "@typescript-eslint/no-explicit-any": "error"
  }
}

```

Like we did with Prettier, we can define two scripts in package.json to work with ESLint:
```
"scripts": {
  "eslint": "eslint 'src/**/*.ts'",
  "eslint:fix": "eslint --fix 'src/**/*.ts'"
}
```
