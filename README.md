# eslint-config-stuff
ES-Lint config stuff

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
