# ngx-select-dropdown

[![GitHub license](https://img.shields.io/github/license/manishjanky/ngx-select-dropdown.svg)](https://github.com/me-and/mdf/blob/master/LICENSE)
[![npm](https://img.shields.io/npm/v/ngx-select-dropdown.svg)]()
[![Build Status](https://travis-ci.org/manishjanky/ngx-select-dropdown.svg?branch=master)](https://travis-ci.org/manishjanky/ngx-select-dropdown)
[![Codecov branch](https://codecov.io/gh/manishjanky/ngx-select-dropdown/branch/master/graphs/badge.svg)]()
[![npm](https://img.shields.io/npm/dt/ngx-select-dropdown.svg)]()
[![GitHub top language](https://img.shields.io/github/languages/top/manishjanky/ngx-select-dropdown.svg)]()
[![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/manishjanky/ngx-select-dropdown.svg)]()
[![GitHub issues](https://img.shields.io/github/issues/manishjanky/ngx-select-dropdown.svg)]()
[![GitHub closed issues](https://img.shields.io/github/issues-closed/manishjanky/ngx-select-dropdown.svg)]()
[![GitHub contributors](https://img.shields.io/github/contributors/manishjanky/ngx-select-dropdown.svg)]()

`ngx-select-dropdown` Custom Dropdown component for Angular 2+ with multiple and single selection options

##Features
* single select dropdown
* multi select dropdown
* search dropdown list

## Examples

* [demo-page](https://manishjanky.github.io/ngx-select-dropdown/)

## Installation

* `npm install ngx-select-dropdown`

### Using with webpack and tsc builds/ angular-cli builds

* import `SelectDropDownModule` into your app.module;
````
import { SelectDropDownModule } from 'ngx-select-dropdown'
````
* add `SelectDropDownModule` to the imports of your NgModule:
`````
@NgModule({
  imports: [
    ...,
    SelectDropDownModule
  ],
  ...
})
class YourModule { ... }
`````

* include css styles in you `angular-cli.json`.

`````
 "styles": [
        "../node_modules/ngx-select-dropdown/dist/assets/style.css"
      ],
`````


* use `<ng--select-dropdown></ng--select-dropdown>` in your templates to add pagination in your view like below

````
<ngx-select-dropdown (change)="selectionChanged($event)" [multiple]="true" [(value)]="dataModel" [config]="config" [options]="dropdownOptions"></ngx-select-dropdown>
````

## Config

### Input

* `multiple: boolean` - `true/false` beased if multiple selection required or not `Defaults to false`.
* `options: Array` - Array of string/objects that are to be the dropdown options.
* `value: any` - the model variable in which you want to save the selected options.
* `config: Object` - configuration object.
````
config = {
        displayKey:"description", //if objects array passed which key to be displayed defaults to description
        search:true //true/false for the search functionlity
      }
````

### Output

* `value: any` - array of selected options
* `change: Event` - change event when user changes the selected options

## Changelog
* v0.1.0
````
 Added a change event so that user can attach a change event handler.
 If multiselect the selected text will display first item and + count for eg. (Option 1 + 2 more) .
````

## Help Improve

Found a bug or an issue with this? [Open a new issue](https://github.com/manishjanky/ngx-select-dropdown/issues) here on GitHub.
