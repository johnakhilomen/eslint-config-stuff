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
