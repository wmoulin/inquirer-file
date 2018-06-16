# inquirer-directory

Relative File prompt for [inquirer](https://github.com/SBoudrias/Inquirer.js)

## Installation

```
npm install --save inquirer-file
```

## Features
- Support for symlinked files
- Vim style navigation
- Search for file with "/" key

### Key Maps
- Press "/" key to enter search mode.
- Press "-" key to go up (back) a directory.

## Usage


This prompt is anonymous, meaning you can register this prompt with the type name you please:

```javascript
inquirer.registerPrompt('file', require('inquirer-file'));
inquirer.prompt({
  type: 'file',
  ...
})
```

Change `file` to whatever you might prefer.

### Options

Takes `type`, `name`, `message`, `basePath`, `ext` properties.

See [inquirer](https://github.com/SBoudrias/Inquirer.js) readme for meaning of all except **basePath** and **ext**.

**basePath** is the relative path from your current working directory
**ext** is the file extension for the file

#### Example

```javascript
inquirer.registerPrompt('file', require('inquirer-file'));
inquirer.prompt([{
  type: 'file',
  name: 'from',
  message: 'Where you like to put this component?',
  basePath: './src',
  ext: '.js'
}], function(answers) {
  //etc
});
```

See also [example.js](https://github.com/nicksrandall/inquierer-file/blob/master/example.js) for a working example

## License

MIT
