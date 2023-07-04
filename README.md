# Ant Design Colors for Scss

English | [简体中文](README.CN.md)

SASS/SCSS implementation for [Ant Design Colors](https://github.com/ant-design/ant-design-colors)

## Install

```shell
npm install ant-design-colors-scss --save-dev
```

## Usage

```scss
@use 'ant-design-colors-scss';
```

Depending on your setup, you may need to configure `node_modules` as `loadPath`:

##### Command-Line

```shell
sass <input.scss> [output.css] --load-path=node_modules
```

##### JavaScript API

```javascript
const sass = require('sass');

sass.compile(filePath, {
  loadPaths: ['node_modules']
});
```

## Example

```scss
@use 'ant-design-colors-scss' as antd-colors;

@debug antd-colors.$blue;
// [#E6F4FF, #BAE0FF, #91CAFF, #69B1FF, #4096FF, #1677FF, #0958D9, #003EB3, #002C8C, #001D66]
@debug antd-colors.$blue-primary;
// #1677FF
@debug antd-colors.$blue-3;
// #91CAFF

@debug antd-colors.$blue-dark;
// [#111A2C, #112545, #15325B, #15417E, #1554AD, #1668DC, #3C89E8, #65A9F3, #8DC5F8, #B7DCFA]
@debug antd-colors.$blue-dark-primary;
// #1668DC
@debug antd-colors.$blue-dark-3;
// #15325B

@debug antd-colors.generate(#1677FF);
// [#E6F4FF, #BAE0FF, #91CAFF, #69B1FF, #4096FF, #1677FF, #0958D9, #003EB3, #002C8C, #001D66]
@debug antd-colors.generate(#1677FF, ('theme': 'dark'));
// [#111A2C, #112545, #15325B, #15417E, #1554AD, #1668DC, #3C89E8, #65A9F3, #8DC5F8, #B7DCFA]

@debug antd-colors.$palette; // Or @debug antd-colors.$palette-dark;
/*
(
  "red"     : [...],
  "volcano" : [...],
  "orange"  : [...],
  "gold"    : [...],
  "yellow"  : [...],
  "lime"    : [...],
  "green"   : [...], 
  "cyan"    : [...], 
  "blue"    : [...], 
  "geekblue": [...],
  "purple"  : [...],
  "magenta" : [...],
  "gray"    : [...]
)
*/
```

## License

[MIT](LICENSE.md) License &copy; 2023-PRESENT [13OnTheCode](https://github.com/13OnTheCode)
