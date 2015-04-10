# DatePicker Plugin for Cordova/PhoneGap 3.0 (iOS and Android)

This is a combined version of DatePicker iOS and Android plugin for Cordova/Phonegap 3.0.
- Original iOS version: https://github.com/sectore/phonegap3-ios-datepicker-plugin

- Original Android version: https://github.com/bikasv/cordova-android-plugins/tree/master/datepicker

## Changes

- uses 24 hour format per default, is also settable by js option (`is24HourView`)
- uses up-to-date theme for date and time picker on android (default to the light theme)
- if js option `clearText` is set to an empty string, it will not be shown in the dialog

## Installation

1) Make sure that you have [Node](http://nodejs.org/) and [Cordova CLI](https://github.com/apache/cordova-cli) or [PhoneGap's CLI](https://github.com/mwbrooks/phonegap-cli) installed on your machine.

2) Add a plugin to your project using Cordova CLI:

```bash
cordova plugin add https://github.com/VitaliiBlagodir/cordova-plugin-datepicker
```
Or using PhoneGap CLI:

```bash
phonegap local plugin add https://github.com/VitaliiBlagodir/cordova-plugin-datepicker
```

## Usage

```js
var options = {
  date: new Date(),
  mode: 'date'
};

datePicker.show(options, function(date){
  alert("date result " + date);  
});
```

## Options

| JS option         	| Description                                                                              	| Type                  	| Options                           	| Default value 	| Supported Plattforms 	|
|-------------------	|------------------------------------------------------------------------------------------	|-----------------------	|-----------------------------------	|---------------	|----------------------	|
| mode              	| The mode of the date picker.                                                             	| String                	| date | time | datetime (ios only) 	| date          	| ios, android         	|
| date              	| Selected date.                                                                           	| String                	|                                   	| new Date()    	| ios, android         	|
| minDate           	| Minimum date                                                                             	| Date | empty String   	|                                   	|               	| ios, android         	|
| maxDate           	| Maximum date                                                                             	| Date | empty String   	|                                   	|               	| ios, android         	|
| clearText         	| If set, a clear button will be shown. Else it is hidden.                                 	| String | empty String 	|                                   	|               	| android (tested)     	|
| is24HourView      	| If date should be shown as 24 hour view                                                  	| boolean               	|                                   	| true          	| android (tested)     	|
| doneButtonLabel   	| Label of done button.                                                                    	| String                	|                                   	| Done          	| ios                  	|
| doneButtonColor   	| Hex color of done button.                                                                	| String                	|                                   	| #0000FF       	| ios                  	|
| cancelButtonLabel 	| Label of cancel button.                                                                  	| String                	|                                   	| Cancel        	| ios                  	|
| cancelButtonColor 	| Hex color of cancel button.                                                              	| String                	|                                   	| #000000       	| ios                  	|
| x                 	| X position of date picker. The position is absolute to the root view of the application. 	| String                	|                                   	| 0             	| ios                  	|
| y                 	| Y position of date picker. The position is absolute to the root view of the application. 	| String                	|                                   	| 0             	| ios                  	|
| minuteInterval    	| Interval between options in the minute section of the date picker.                       	| Integer               	|                                   	| 1             	| ios                  	|
| allowOldDates     	| Shows or hide dates earlier then selected date.                                          	| Boolean               	|                                   	| true          	| ios                  	|
| allowFutureDates  	| Shows or hide dates after selected date.                                                 	| Boolean               	|                                   	| true          	| ios                  	|

## Requirements
- PhoneGap 3.0 or newer / Cordova 3.0 or newer
- Android 2.3.1 or newer / iOS 5 or newer

## Example

```js
var options = {
  date: new Date(),
  mode: 'date'
};

datePicker.show(options, function(date){
  alert("date result " + date);  
});
```
